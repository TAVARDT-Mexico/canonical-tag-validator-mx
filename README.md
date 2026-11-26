<p align="center">
  <a href="https://ag.tavardt.com/mx/">
    <img src="https://ag.tavardt.com/img/tavardt-banner.png" alt="TAVARDT" width="1024" />
  </a>
</p>

# Validador de Etiquetas Canonicas y Consolidacion de URLs

[![Validador Etiqueta Canonica](https://img.shields.io/badge/TAVARDT-Canonical-5b3cf5.svg)](https://tools.tavardt.com/mx/validador-etiqueta-canonica/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditoria de enlaces canonicos, deteccion de etiquetas duplicadas, verificacion de URLs absolutas y eficiencia de rastreo.

Desarrollado y mantenido por la division de ingenieria de indexacion e infraestructura de busqueda de **TAVARDT**.

***

## Vectores de Riesgo e Impacto Operativo en la Consolidacion de URLs

El mal uso de etiquetas canonicas induce canibalizacion organica y desaprovechamiento de rastreo en plataformas digitales. La dispersion generada por cadenas de consulta y filtros dinamicos debilita la posicion del dominio en Google.

Si las anotaciones canonicas resultan contradictorias o apuntan a paginas no disponibles, los motores de busqueda anulan la directiva. La verificacion tecnica continua asegura que la relevancia se concentre en las paginas oficiales.

***

## Capacidades Centrales de Auditoria Tecnica

* **Extraccion de Directivas en Fuente Doble**: Analisis exhaustivo de etiquetas canonicas en el marcado HTML y en encabezados HTTP Link del servidor.
* **Prevencion de Etiquetas Multiples en Conflicto**: Deteccion de declaraciones contradictorias en un mismo documento, deduciendo 35 puntos por ambiguedad.
* **Validacion de URL Absoluta y HTTPS**: Verificacion de rutas completas y penalizacion inmediata ante rutas relativas o uso de protocolo inseguro HTTP.
* **Comprobacion Activa de Respuesta del Destino**: Verificacion en vivo del estado HTTP del enlace canonico para interceptar codigos de error 4xx o 5xx.
* **Analisis de Autorreferencia y Consolidacion**: Comprobacion de enlaces autorreferenciales para depurar parametros dinamicos y rastros de sesion.
* **Puntuacion de Salud de Consolidacion**: Metrica tecnica de 0 a 100 clasificando el activo en COMPLIANT, WARNING o CRITICAL.

***

## Instalacion y Ejecucion

Requiere Python 3.8 o superior sin librerias adicionales.

```bash
git clone https://github.com/TAVARDT-Mexico/canonical-tag-validator-mx.git
cd canonical-tag-validator-mx
python canonical_validator.py https://empresa.com.mx
```

Para generar la salida en formato JSON estructurado en flujos de integracion continua:

```bash
python canonical_validator.py https://empresa.com.mx -j
```

***

## Preguntas Frecuentes (FAQ Tecnico)

### 1. Que sucede si se declaran multiples etiquetas canonicas contradictorias en una pagina?
Los buscadores descartan la totalidad de las directivas canonicas cuando detectan instrucciones enfrentadas en una misma URL. Como resultado, los rastreadores eligen aleatoriamente que version indexar, fragmentando la autoridad del portal.

### 2. Por que la URL canonica debe especificarse de forma absoluta y bajo protocolo HTTPS?
Las rutas relativas son susceptibles de interpretaciones erroneas al navegar entre diferentes subdominios o directorios raiz. Asimismo, el uso de HTTP inseguro genera advertencias de seguridad y saltos de redireccion innecesarios.

### 3. Cual es el riesgo operativo de apuntar una etiqueta canonica a una URL con error 4xx o 5xx?
Apuntar una directiva canonica a un destino que devuelve un error HTTP anula el proceso de consolidacion. Google ignora el destino inaccesible y pasa a indexar versiones duplicadas con parametros de rastreo.

### 4. La herramienta inspecciona encabezados HTTP Link ademas del codigo HTML?
Si, el analizador procesa tanto las etiquetas del marcado HTML como los encabezados HTTP Link transmitidos por el servidor. Esto permite auditar la consolidacion canonica de recursos no basados en HTML como documentos PDF.

### 5. Como protegen las etiquetas autorreferenciales contra la dispersion por parametros?
Una etiqueta canonica autorreferencial limpia instruye a los rastreadores para ignorar variables de campana y codigos de sesion. De este modo, se concentra la autoridad en la ruta oficial y se protege el presupuesto de rastreo.

***

## Consultoria en SEO Tecnico e Indexacion de Portales

Para planificacion de arquitecturas web multirregionales y cumplimiento de estandares W3C, consulte al equipo de **TAVARDT**.

***

## Enlaces Utiles

* **Portal Corporativo:** https://ag.tavardt.com/mx/
* **Suite de Diagnosticos:** https://tools.tavardt.com/mx/
* **Contacto Tecnico:** https://ag.tavardt.com/mx/contacto/

***

### Licencia
Distribuido bajo la Licencia MIT. Consulte el archivo LICENSE para conocer los terminos completos.

***

© 2026 TAVARDT. Todos los derechos reservados.
