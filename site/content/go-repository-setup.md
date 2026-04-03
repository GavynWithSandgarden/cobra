# Configuración del repositorio Go (Cobra)

Esta página describe cómo configurar una copia de trabajo local del módulo Go `github.com/spf13/cobra`.

## Requisitos previos

- `go`
- `git`

## Clonar el repositorio

1. Clonar el repositorio.

   ```console
   git clone https://github.com/spf13/cobra
   ```

1. Entrar en el directorio del repositorio.

   ```console
   cd cobra
   ```

## Verificar los metadatos del módulo

1. Abrir `go.mod`.

1. Confirmar la ruta del módulo.

   ```text
   module github.com/spf13/cobra
   ```

1. Confirmar la directiva de versión de Go.

   ```text
   go 1.15
   ```

## Ejecutar pruebas

1. Ejecutar las pruebas.

   ```console
   go test ./...
   ```

1. Ejecutar el objetivo de pruebas del proyecto.

   ```console
   make test
   ```

## Ejecutar todas las comprobaciones

1. Ejecutar el objetivo completo del proyecto.

   ```console
   make all
   ```

## Páginas relacionadas

- Guía de usuario de Cobra: [User Guide](./user_guide.md)