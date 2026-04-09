
Cobra es una biblioteca para crear potentes y modernas aplicaciones de línea de comandos (CLI).

Visita Cobra.dev para documentación detallada de Cobra.


Cobra se utiliza en muchos proyectos de Go, como Kubernetes,
Hugo y GitHub CLI, entre otros.
[Esta lista](site/content/projects_using_cobra.md) contiene un listado más amplio de proyectos que usan Cobra.

<hr>

# Descripción general

Cobra es una biblioteca que proporciona una interfaz sencilla para crear potentes y modernas interfaces de línea de comandos (CLI)
similares a las herramientas `git` y `go`.

Cobra proporciona:
* CLI basadas en subcomandos de forma sencilla: `app server`, `app fetch`, etc.
* Flags totalmente compatibles con POSIX (incluidas las versiones cortas y largas).
* Subcomandos anidados.
* Flags globales, locales y en cascada.
* Sugerencias inteligentes (`app srver`... ¿quiso decir `app server`?).
* Generación automática de ayuda para comandos y flags.
* Agrupación de la ayuda para subcomandos.
* Reconocimiento automático de flags de ayuda como `-h`, `--help`, etc.
* Autocompletado de shell generado automáticamente para tu aplicación (bash, zsh, fish, PowerShell).
* Páginas de _man_ generadas automáticamente para tu aplicación.
* Alias de comandos para que puedas cambiar cosas sin romper la compatibilidad.
* Flexibilidad para definir tu propia ayuda, uso, etc.
* Integración opcional y transparente con la biblioteca `viper` para aplicaciones de 12 factores.

# Conceptos

Cobra se basa en una estructura de comandos, argumentos y flags.

**Commands** (comandos) representan acciones, **Args** (argumentos) son cosas y **Flags** (banderas) son modificadores de esas acciones.

Las mejores aplicaciones se leen como frases cuando se usan y, como resultado,
las personas saben de forma intuitiva cómo interactuar con ellas.

El patrón a seguir es
`APPNAME VERB NOUN --ADJECTIVE`
    o
`APPNAME COMMAND ARG --FLAG`.

Algunos buenos ejemplos del mundo real pueden ilustrar mejor este punto.

En el siguiente ejemplo, `server` es un comando y `port` es un flag:

    hugo server --port=1313

En este comando le estamos diciendo a Git que clone la URL en modo _bare_.

    git clone URL --bare

## Comandos

`Command` es el punto central de la aplicación. Cada interacción que
la aplicación admite estará contenida en un `Command`. Un comando puede
tener comandos hijo y opcionalmente ejecutar una acción.

En el ejemplo anterior, `server` es el comando.

Para más información, consulta la documentación de `cobra.Command` en el paquete.

## Banderas (flags)

Un flag es una forma de modificar el comportamiento de un comando. Cobra admite
flags totalmente compatibles con POSIX, así como el paquete estándar `flag` de Go.
Un comando de Cobra puede definir flags que se propaguen a los comandos hijo
y flags que solo estén disponibles para ese comando.

En el ejemplo anterior, `port` es el flag.

La funcionalidad de las flags la proporciona la biblioteca `pflag`, un _fork_ de la biblioteca estándar `flag`
que mantiene la misma interfaz y añade compatibilidad con POSIX.


# Instalación
Usar Cobra es sencillo. Primero, utiliza `go get` para instalar la última versión
de la biblioteca.

```
go get -u github.com/spf13/cobra@latest
```

Después, incluye Cobra en tu aplicación:

```go
import "github.com/spf13/cobra"
```
# Uso
`cobra-cli` es un programa de línea de comandos para generar aplicaciones y archivos de comando basados en Cobra.
Generará el andamiaje (_scaffolding_) de tu aplicación para desarrollar rápidamente
una aplicación basada en Cobra. Es la manera más sencilla de incorporar Cobra a tu aplicación.

Se puede instalar ejecutando:

```
go install github.com/spf13/cobra-cli@latest
```

Para obtener todos los detalles sobre el uso del generador Cobra-CLI, lee el archivo README de Cobra-CLI.

Para obtener todos los detalles sobre el uso de la biblioteca Cobra, lee la [Guía de usuario de Cobra](site/content/user_guide.md).

# Licencia

Cobra se distribuye bajo la licencia Apache 2.0. Consulta [LICENSE.txt](LICENSE.txt).
