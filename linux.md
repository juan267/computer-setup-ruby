# Instrucciones de configuración para Linux

**Nota**: Estas instrucciones están optimizadas para `Ubuntu`. Si estas usando una versión diferente de Linux es posible que tengas que traducir estos comandos para tu OS en particular.

## Paso 1: Actualiza el package manager

El primer paso es asegurarnos que tienes que `apt-get` este actualizado. Esto se hace con el siguiente comando:

```bash
  $ sudo apt-get update
```

Si no salio ningun error podemos ahora instalar `curl`:

```bash
  $ sudo apt-get curl
```

Si eso no funciona es posible que tengas que intentar:

```bash
  $ sudo apt-get install curl
```

Ahora estas listo para instalar `Rbenv`

## Paso 2: Instala Rbenv

Rbenv va a ser tu administrador de versiones para Ruby. Digital Ocean escribió una guiá sobre como hacer esto en Ubuntu, sigue las instrucciones que se encuentran [aca](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-14-04). Esto tambien cubre instalar `nodejs` y `git`. Instala ruby `2.3.3` en vez de `2.2.3`.

El paso de abrir el `bashrc` y modificar el `PATH` se hacen en la paso 3 de esta guia de modo que no es necesario que los completes por ahora.


## Paso 3: Configura tu Path

Lo que vamos hacer es modificar el archivo que configura la apariencia y funcionamiento de tu terminal. Esto sucede al configurar el archivo de tu computador llamado `.bashrc`. Con estos cambios tu terminal queda integrada con `git` se habilita el auto completado usando `tab`, pruebas de `rspec` salen con colores.

Vamos a clonar un repositorio de Github que contiene el código que queremos usar y luego lo vamos a instalar. Sigue los siguientes pasos cada paso es un comando independiente:

```bash
  $ git clone https://github.com/supertopher/dotfiles.git
```

```bash
  $ cd dofiles
```

```bash
  $ ./install
```

Reinicia la terminal para que los cambios tengan efecto.

## Paso 4: Instala Git

Esto debió suceder mientras seguías las instrucciones de `Digital Ocean` en el paso 2. Puedes verificar que ya este instalado con este comando:

```bash
  $ git --version
```

## Paso 5: Configura Git

Necesitamos sobrescribir el archivo `.gitconfig` para que contenga tu usuario y contraseña de `Github`. Usa tu nombre y tu correo de Github en los siguientes comandos:

```bash
  $ git config --global user.name 'Pepito Perez'
  $ git config --global user.email 'pepito.perez@example.com'
```

## Paso 6: Configura Sublime

Este comando configura Sublime como tu editor predeterminado de git

Ejecuta este comando para agregar el comando `subl` a tu terminal:

```bash
  $ sudo ln -s /opt/sublime_text/sublime_text /usr/local/bin/subl
```

```bash
  $ git config --global core.editor "subl -w"
```

## Paso 7: Instala Node

Node te permite correr Javascript en tu terminal. Esto debió suceder mientras seguías las instrucciones de `Digital Ocean` en el paso 2. Puedes verificar que ya este instalado con este comando:

```bash
  $ node -v
```

## Paso 8: Instala SQlite

Instala SQlite usando `apt-get`. Ejecuta el comando:

```bash
  $ sudo apt-get install sqlite3 libsqlite3-dev
```

y luego..

```bash
  $ gem install sqlite3-ruby
```

prueb que quedo bien instalado con el comando

```bash
  $ sqlite3 --version
```

## Paso 9: Instala Postgres

Escribe los siguientes comandos:

```bash
  $ sudo apt-get install postgresql
```

Sigue las instrucciones que te salen en la pantalla.

Puedes verificar que quedo bien instalado con el comando

```bash
  $ psql -V
```
