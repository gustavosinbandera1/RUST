# Table of Contents
- [Table of Contents](#table-of-contents)
  - [Instalacion](#instalacion)
  - [Herramientas](#herramientas)
    - [rustup](#rustup)
  - [Comandos](#comandos)
    - [Instalar](#instalar)
    - [Actualizar todas las versiones instaladas](#actualizar-todas-las-versiones-instaladas)
    - [Actualizar una version especifica](#actualizar-una-version-especifica)
    - [Especificar version por defecto](#especificar-version-por-defecto)
    - [Especificar versión para un proyecto](#especificar-versi%c3%b3n-para-un-proyecto)
    - [rustc](#rustc)


## Instalacion
Para instalar Rust, los usuarios de GNU/Linux y MacOS deben ejecutar el siguiente comando desde la terminal:

```bash
$ curl https://sh.rustup.rs -sSf | sh
```

Con el comando anterior iniciamos la descarga de l instalador de Rust llamdo ```rustup```, el cual instala la versiona mas estable del lenguaje, que incluye el compilador (rustc) y Cargo (gestor de paquetes).

En Arch Linux y derivados, rustup está disponible desde los repositorios oficiales por lo que puede instalarse usando pacman:

```bash
$ sudo pacman -S rustup
```

## Herramientas

### rustup

rustup es el instalador de Rust y la herramienta con la que pueden gestionarse las diferentes versiones de Rust instaladas. 

El lenguaje sigue un ciclo de desarrollo muy similar al de Firefox, por lo que cada seis semanas se publica una versión nueva. La última versión estable.

En Rust existen tres canales de actualización: Stable, Beta y Nightly. Algunos frameworks como Rocket (un framework para desarrollo web) ocupan la versión Nightly.

## Comandos

### Instalar

```bash
$ rustup install nightly
```

### Actualizar todas las versiones instaladas

```bash
$ rustup update
```

### Actualizar una version especifica

```bash
$ rustup update nightly
```

### Especificar version por defecto

```bash
$ rustup default stable
```

### Especificar versión para un proyecto

```bash
$ rustup override set nightly
```

### rustc

Se trata del compilador del lenguaje. Los archivos que contienen código fuente de Rust llevan la extensión .rs, y su estructura es la siguiente:

```rust
fn main() {
      println!("Hello, world!");
  }
```

Se guarda el código anterior en un archivo llamado main.rs, o el nombre que se le quiera dar, y para ejecutar el programa se escriben los siguientes comandos en la terminal, desde la ruta donde se haya guardado el archivo:

```bash
$ rustc main.rs
$ ./main
Hello, world!
```