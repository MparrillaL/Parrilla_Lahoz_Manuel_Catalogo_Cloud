# Catálogo Cloud - Versión 2

## Descripción
Esta es la **versión 2** de los archivos de catálogo cloud para el módulo LMSGI (Lenguajes de Marcas y Gestión de Información) del CFGS DAM/DAW.

## Contenido

### Archivos incluidos
- **CatalogoCloud_v2.xml** - Documento XML con la estructura de infraestructura cloud
- **CatalogoCloud_v2.xsd** - Esquema XSD que valida la estructura y format del XML

## Sobre los archivos

### CatalogoCloud_v2.xml
Contiene datos de centros de datos distribuidos geográficamente:
- **Centro de Datos Madrid** (eu-sur-1)
  - srv-web-01: Servidor web con Nginx
  - srv-db-01: Servidor de base de datos PostgreSQL
  
- **Centro de Datos París** (eu-centro-1)
  - srv-ia-01: Servidor de IA/ML con GPU NVIDIA A100
  - srv-backup-01: Servidor de backup con almacenamiento masivo

### CatalogoCloud_v2.xsd
Esquema con validación mediante patrones RegEx que asegura:
- IDs de servidor con formato: `srv-[letras]-[2 dígitos]`
- Zonas geográficas: `[2 letras]-[letras]-[número]`
- Racks: `[Mayúscula][1-2 dígitos]`
- Estados válidos: activo, mantenimiento, apagado
- Tipos de disco válidos: NVMe, SSD, HDD
- Unidades de almacenamiento válidas: MB, GB, TB

## Validación
Para validar el archivo XML contra el esquema XSD, puede utilizarse cualquier herramienta de validación XML estándar.

## Autor
Manuel Parrilla Lahoz

## Módulo
LMSGI - CFGS DAW
