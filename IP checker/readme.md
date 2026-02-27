## checkip

Herramienta CLI para consultar información de direcciones IP directamente desde la terminal.

Utiliza la API de IPinfo (HTTPS) para obtener:

- País
- Región
- Ciudad
- Organización / ISP
- Detección de IP privada (bogon)

---

## Requisitos

- macOS (probado en zsh)
- curl
- jq

Instalar jq si no está presente:

## Configuración

Editar el archivo checkip y colocar tu API Token:
API_TOKEN="TU_TOKEN_AQUI"

Obtener token en:
https://ipinfo.io

## Instalación

Dar permisos de ejecución:
chmod +x checkip

## Uso 

IP simple
checkip 8.8.8.8

Varias IPs en una línea
checkip 8.8.8.8 1.1.1.1

Texto con fechas y comentarios
checkip "123.123.123.123 # 2025-11-03 17:18:55 -0500 186.114.224.109 # 2025-11-09"

## Ejemplo de salida
123.123.123.123
País: CO | Región: Santander | Ciudad: Bucaramanga | Org: AS3816 COLOMBIA TELECOMUNICACIONES S.A.

123.123.123.123
País: CO | Región: Antioquia | Ciudad: Medellín | Org: Claro Colombia

## Características

Extrae automáticamente IPs válidas
Elimina duplicados
Ignora texto adicional (# comentarios, fechas, etc.)
Detecta IPs privadas/reservadas
Funciona con argumentos o STDIN
Timeout de conexión configurado
Solo usa HTTPS
