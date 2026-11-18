# Caso Novapay · La evidencia del servidor

Laboratorio de la Clase 5 del curso de Ciberseguridad: primeros pasos en la terminal de Linux con un objetivo de analista. Los datos son inventados y las IP pertenecen a rangos reservados para documentación (RFC 5737).

**El caso.** La cuenta `soporte` cambió la página de inicio del sitio de Novapay durante la madrugada y nadie del equipo lo hizo. Con el registro de inicios de sesión del servidor, respondé: ¿alguien accedió sin autorización?, ¿desde qué IP? y ¿con qué cuenta?

## Cómo empezar

Abrí una terminal de Linux (por ejemplo, [Google Cloud Shell](https://shell.cloud.google.com), gratis con una cuenta de Google) y ejecutá:

```
wget https://lfjuarez.github.io/novapay/caso-novapay.zip
sha256sum caso-novapay.zip
```

El hash tiene que ser:

```
895ea610266e80fd8b76ffcc5a7a77520d0e768d3b2ed973b0e0f396a6dc4970  caso-novapay.zip
```

Seguí los 10 pasos de la guía: [guia.pdf](guia.pdf).

## Contenido

| Archivo | Qué es |
|---|---|
| `caso-novapay.zip` | La evidencia: `auth.log`, `notas.txt` y `usuarios.txt` |
| `caso-novapay.zip.sha256` | El hash publicado, para verificar la descarga |
| `guia.pdf` | La guía paso a paso |
| `hoja-de-comandos.pdf` | Los comandos de la clase en una página |
| `practica.zip` | Archivos para practicar los comandos básicos (el video de comandos los usa) |

Usalo solo para aprender: escaneá y probá únicamente en tus equipos o con permiso escrito.
