# Caso Novapay · La evidencia del servidor

Laboratorio de la Clase 5 del curso de Ciberseguridad: primeros pasos en la terminal de Linux con un objetivo de analista. Los datos son inventados. La IP del atacante, 45.140.192.242, es real: está reportada públicamente por ataques de fuerza bruta contra SSH (AbuseIPDB, GreyNoise, VirusTotal) y la usamos para practicar cómo se investiga una IP. El ataque a Novapay es ficticio. Las demás IP externas pertenecen a rangos reservados para documentación (RFC 5737).

**El caso.** La cuenta `soporte` cambió la página de inicio del sitio de Novapay durante la madrugada y nadie del equipo lo hizo. Con el registro de inicios de sesión del servidor, respondé: ¿alguien accedió sin autorización?, ¿desde qué IP? y ¿con qué cuenta?

## Cómo empezar

Abrí una terminal de Linux (por ejemplo, [Google Cloud Shell](https://shell.cloud.google.com), gratis con una cuenta de Google) y ejecutá:

```
wget https://lfjuarez.github.io/novapay/caso-novapay.zip
sha256sum caso-novapay.zip
```

El hash tiene que ser:

```
ae454dbcae839ef4b7a2e0e2166b8405f401dbfdf837f646b1a7396c32f654cd  caso-novapay.zip
```

Seguí los 11 pasos de la guía: [guia.pdf](guia.pdf). Si nunca usaste una terminal, mirá antes el video [Linux para analistas · Comandos básicos uno por uno](https://youtu.be/AKh9FE14jzs) (7 minutos). Si te trabás, el video [Lab Caso Novapay resuelto](https://youtu.be/JzuwpTv-mPk) muestra los 11 pasos.

## Parte 2 · Contención y hardening del servidor (Clase 6)

El atacante accedió con la cuenta `soporte`. ¿Qué dejó en el servidor para volver? Investigá la persistencia, cortá el acceso y endurecé la configuración en tu propio Cloud Shell:

```
wget https://lfjuarez.github.io/novapay/caso-servidor.zip
sha256sum caso-servidor.zip
```

El hash tiene que ser:

```
6e3d97ebe748f7d8e484101df9c9b652c6f2b1e0245a7fcbaa89d56625840f94  caso-servidor.zip
```

Seguí los 11 pasos de la guía: [guia-servidor.pdf](guia-servidor.pdf). Leé `preparar.sh` antes de ejecutarlo con `sudo`: solo cambia tu máquina de práctica de Cloud Shell, no envía nada a internet ni reinicia SSH, y las contraseñas de los usuarios de ejemplo se generan al azar, sin mostrarse. Al final, `sudo bash verificar.sh` comprueba los siete controles y te da un código de verificación único para tu usuario de Cloud Shell: entregá el código y el usuario.

Video con los 10 pasos resueltos: [Lab Caso Novapay · Parte 2 resuelto](https://youtu.be/SP-O6zvebMM). Después de intentarlo, compará con [respuestas-servidor.pdf](respuestas-servidor.pdf).

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
