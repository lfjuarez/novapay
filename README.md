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

Seguí los 10 pasos de la guía: [guia.pdf](guia.pdf). Si nunca usaste una terminal, mirá antes el video [Linux para analistas · Comandos básicos uno por uno](https://youtu.be/AKh9FE14jzs) (7 minutos). Si te trabás, el video [Lab Caso Novapay resuelto](https://youtu.be/POC5iLnjFTE) muestra los 10 pasos.

## Parte 2 · Contención y hardening del servidor (Clase 6)

El atacante accedió con la cuenta `soporte`. ¿Qué dejó en el servidor para volver? Investigá la persistencia, cortá el acceso y endurecé la configuración en tu propio Cloud Shell:

```
wget https://lfjuarez.github.io/novapay/caso-servidor.zip
sha256sum caso-servidor.zip
```

El hash tiene que ser:

```
324c279d88a99fe6fcd95d96c40345a878052b5d881314e8f53e3367c45b4f11  caso-servidor.zip
```

Seguí los 10 pasos de la guía: [guia-servidor.pdf](guia-servidor.pdf). Leé `preparar.sh` antes de ejecutarlo con `sudo`: solo cambia tu máquina de práctica de Cloud Shell, no envía nada a internet y todo se borra al reiniciarla. Al final, `sudo bash verificar.sh` comprueba los siete controles.

Video con los 10 pasos resueltos: [Lab Caso Novapay · Parte 2 resuelto](https://youtu.be/n20AkyxLG00). Después de intentarlo, compará con [respuestas-servidor.pdf](respuestas-servidor.pdf).

## Contenido

| Archivo | Qué es |
|---|---|
| `caso-novapay.zip` | La evidencia: `auth.log`, `notas.txt` y `usuarios.txt` |
| `caso-novapay.zip.sha256` | El hash publicado, para verificar la descarga |
| `guia.pdf` | La guía paso a paso |
| `hoja-de-comandos.pdf` | Los comandos de la clase en una página |
| `practica.zip` | Archivos para practicar los comandos básicos (el video de comandos los usa) |
| `caso-servidor.zip` | Parte 2: `preparar.sh`, `verificar.sh` y `notas-servidor.txt` |
| `caso-servidor.zip.sha256` | El hash publicado de la Parte 2 |
| `guia-servidor.pdf` | La guía de la Parte 2 |
| `respuestas-servidor.pdf` | Lo que tenía que aparecer en cada paso y las respuestas sugeridas de la Parte 2 |

Usalo solo para aprender: escaneá y probá únicamente en tus equipos o con permiso escrito.
