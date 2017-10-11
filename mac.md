# Instrucciones de configuración para Mac

## Paso 1: Instalar las herramientas de linea de comandos

Ejecuta el siguiente comando en la terminal:

```bash
  $ xcode-select --install
```

Sigue los pasos que te indica el `prompt` para terminar la instalación. Esto va a instalar el compilador de `C` de Apple el cual te permite apps nativas desde su fuente (ej Ruby)

## Paso 2: Instala Homebrew

También conocido como `brew`. Brew es como el App store de la linea de comandos. Cuando necesites alguna herramienta para la terminal, intenta instalar usando Brew antes de usar otros metodos. Ej: (`brew install nombre-de-la-cosa`)

Para instalar brew ejecuta el siguiente comando en la terminal:

```bash
  $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Te va a pedir tu password de modo que tenlo preparado.


## Paso 3: Configura tu Path

Lo que vamos a hacer es modificar el archivo que configura la apariencia y funcionamiento de tu terminal. Esto sucede al configurar el archivo de tu computador llamado `.bash_profile`. Con estos cambios tu terminal queda integrada con `git` se habilita el auto completado usando `tab`, pruebas de `rspec` salen con colores, y configura el comando `subl` como atajo para abrir sublime.

Primero clona un repositorio de Github que contiene el código que queremos usar y luego lo vamos a instalar. Sigue los siguientes pasos cada paso es un comando independiente:

```bash
  $ git clone https://github.com/supertopher/dotfiles.git
```

```bash
  $ cd dotfiles
```

```bash
  $ ./install
```

## Paso 4: Configura Git

Necesitamos sobrescribir el archivo `.gitconfig` para que contenga tu usuario y contraseña de `Github`. Usa tu nombre y tu correo de Github en los siguientes comandos:

```bash
  $ git config --global user.name 'Pepito Perez'
  $ git config --global user.email 'pepito.perez@example.com'
```

## Paso 5: Configura Sublime

Este comando configura Sublime como tu editor predeterminado de git

```bash
  $ git config --global core.editor "subl -w"
```

## Paso 6: Instala Rbenv

Rbenv es el administrador de versiones de ruby para tu computador. Te permite tener varias versiones de ruby instaladas y saltar de una a otra fácilmente. Ejecuta los siguientes comandos para instalarlo:

```brew
  $ brew install rbenv
```

**Nota**: Si ya tienes instalado `RVM`. NO tienes que instalar Rbenv. No intentes instalar ambos, no funcionan bien juntos y seguramente harán un lio de tu maquina. Rbenv es mi método preferido, de modo que si quieres instalarlo debes primero asegurarte de haber des instalado RVM.

## Paso 7: Instala Ruby Build

Rbenv usa internamente este programa para manejar las versiones de Ruby.

```bash
  brew install ruby-build
```

## Paso 8: Instala Ruby 2.3.3

Ejecuta el comando

```bash
 $ rbenv install 2.3.3
```

Ahora necesitas configurar la versión de ruby que quieres usar por default, a la que acabamos de instalar. Ejecuta el comando:

```bash
  $ rbenv global 2.3.3
```

**Reinicia tu terminal**

## Paso 9: Instala Git

Ejecuta el comando

```bash
 $ brew install git
```

## Paso 10: Instal Node

Node te permite correr Javascript en tu terminal. Ejecuta el siguiente comando:

```bash
  brew install node
```

## Paso 11: Instala SQlite

Ejecuta el comando:

```bash
  $ brew install SQlite3
```

Para sobrescribir la copia del sistema de SQlite, tenemos que escribir este comando:

```bash
  $ brew link sqlite3 --force
```
## Paso 12: Instala Postgres

Sigue las instrucciones para instalar [Postgres App](https://postgresapp.com/).













