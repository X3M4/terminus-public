# Terminus · zonas geográficas

Paquetes de zona públicos de Terminus (Nova Cartografía): catálogo de sistemas de referencia y
rejillas de geoide de cada zona. Terminus los descarga a petición del usuario o los instala desde
fichero, y antes de instalarlos comprueba el SHA-256 fijado en su código y la firma minisign.

Los paquetes están en las [Releases](https://github.com/X3M4/terminus-public/releases) de este
repositorio, cada uno con su firma `.minisig` al lado.

| Zona | Release | SRC | Rejillas | SHA-256 del zip |
|---|---|---|---|---|
| Estados Unidos (continental) | `zone-us-1` | NAD83(2011) / UTM 10N–19N + NAVD88 | GEOID18 `us_noaa_g2018u0.tif` (NOAA NGS, dominio público) | `d144539e23ee82bea72801615cf0b0d722909c5baa0d2c0f38cf4cd016e02af6` |

Las rejillas proceden de [PROJ-data](https://github.com/OSGeo/PROJ-data) 1.24; la licencia y la
atribución de cada una van dentro del paquete (`licenses/`).

## Verificar a mano

Clave pública minisign de confianza (2E62ACDC36617D24):

```
RWQkfWE23KxiLirgqTRLHRS0+vbYfBiaLkZx/onLhlqjCk25Ux6ntAMI
```

```sh
minisign -Vm zone-us-1.zip -P RWQkfWE23KxiLirgqTRLHRS0+vbYfBiaLkZx/onLhlqjCk25Ux6ntAMI
sha256sum zone-us-1.zip
```
