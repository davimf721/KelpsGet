# Registro de Cambios

[English](../CHANGELOG.md) | [Português](CHANGELOG.pt-BR.md) | [Español](CHANGELOG.es.md)

Todos los cambios notables en este proyecto serán documentados en este archivo.

El formato está basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/),
y este proyecto adhiere a [Versionado Semántico](https://semver.org/lang/es/).

## [0.1.4] - 2025-05-22

### Añadido
- Interfaz Gráfica de Usuario (GUI) para descargas más fáciles.
- Soporte para descarga vía FTP.
- Soporte para descarga vía SFTP (autenticación basada en contraseña y clave).
- Soporte para descarga de Torrent vía enlaces magnéticos (se integra con el demonio Transmission).
- Instrucciones detalladas para la configuración del demonio Transmission en el README.

### Cambiado
- Refinada la determinación de la ruta de salida para alinear el comportamiento con `wget`.
- Asegurado que `final_path` sea siempre absoluto para prevenir errores de "No existe el fichero o el directorio" en el CWD (directorio de trabajo actual).
- Actualizado el README en Inglés, Portugués y Español para reflejar todas las nuevas características e instrucciones de configuración.

### Corregido
- Resuelto error "No existe el fichero o el directorio" al descargar sin `-O`, asegurando rutas absolutas.
- Corregido `validate_filename` para verificar solo el nombre base del archivo, no la ruta completa.
- Abordados problemas potenciales con `map_err` en `main.rs` para descargas de torrent y HTTP.

## [0.1.3] - 2025-03-11

### Añadido
- Modo de descarga avanzado con chunks paralelos y capacidad de reanudación
- Soporte de compresión automática (gzip, brotli, lz4)
- Sistema de caché inteligente para descargas repetidas más rápidas
- Limitación de velocidad y control de conexión
- Soporte de documentación en múltiples idiomas

### Cambiado
- Mejorado el manejo de errores y retroalimentación al usuario
- Mejorada la barra de progreso con información más detallada
- Optimizado el uso de memoria para descargas de archivos grandes
- Actualizado el sistema de configuración de proxy

### Corregido
- Corregidos problemas de autenticación de proxy
- Resueltos problemas de creación de directorio de caché
- Corregido el manejo de niveles de compresión
- Corregido el manejo de rutas de archivo en Windows

### Seguridad
- Añadido manejo seguro de conexiones proxy
- Mejorada la validación de URLs
- Mejorada la sanitización de nombres de archivo
- Añadida verificación de espacio antes de las descargas

## [0.1.2] - 2025-03-10

### Añadido
- Soporte de proxy (HTTP, HTTPS, SOCKS5)
- Autenticación de proxy
- Nombrado personalizado de archivos de salida
- Detección de tipo MIME

### Cambiado
- Mejorado el cálculo de velocidad de descarga
- Mejorada la visualización de la barra de progreso
- Mejores mensajes de error
- Documentación actualizada

### Corregido
- Corregidos problemas de timeout de conexión
- Resueltos problemas de permisos de archivos
- Corregido el análisis de URLs
- Corregida la visualización de la barra de progreso en Windows

## [0.1.1] - 2025-03-09

### Añadido
- Modo silencioso para integración con scripts
- Barra de progreso básica
- Visualización del tamaño del archivo
- Monitoreo de velocidad de descarga

### Cambiado
- Mejorado el manejo de errores
- Mejorada la interfaz de línea de comandos
- Mejor manipulación de archivos
- Actualizadas las instrucciones de instalación

### Corregido
- Corregidos problemas de manejo de rutas
- Resueltos problemas de permisos
- Corregida la visualización de progreso
- Corregido el comportamiento de sobrescritura de archivos

## [0.1.0] - 2025-03-08

### Añadido
- Lanzamiento inicial
- Funcionalidad básica de descarga de archivos
- Interfaz de línea de comandos
- Manejo básico de errores
- Soporte multiplataforma