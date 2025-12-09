# 🌍 Actividad 2 — “Exploradores Remotos”
### Duración aproximada: 20 minutos  
### Objetivo: Aprender a trabajar con ramas remotas en Git (en GitHub u otro servidor), sin utilizar todavía Pull Requests.

---

## 🧰 1. Antes de empezar

Antes de comenzar esta actividad, asegúrate de:

- Haber completado la Actividad 1.
- Tener el repositorio abierto en VS Code o en tu editor favorito.
- Tener correctamente configurado el remoto `origin` (normalmente GitHub).

Puedes verificarlo ejecutando:

```bash
git remote -v
```

Debe aparecer algo similar a:

```
origin  https://github.com/tu-usuario/tu-repo.git (fetch)
origin  https://github.com/tu-usuario/tu-repo.git (push)
```

---

## 🚀 2. Sube tu rama creativa al remoto

En la Actividad 1 creaste una rama local con un nombre divertido.  
Ahora la vas a subir a GitHub para que otros compañeros puedan explorarla.

### 2.1. Comprueba en qué rama estás

```bash
git branch
```

Si no estás en tu rama creativa, cámbiate:

```bash
git switch nombre-de-tu-rama
```

### 2.2. Sube la rama al remoto por primera vez

Usa este comando:

```bash
git push -u origin nombre-de-tu-rama
```

El parámetro `-u` vincula tu rama local con la rama remota, de forma que a partir de ahora podrás usar simplemente:

```bash
git push
git pull
```

---

## 🔭 3. Ver las ramas remotas

Ahora que todas las personas han subido sus ramas, es momento de explorarlas.

### 3.1. Actualiza la información del remoto

```bash
git fetch
```

Este comando **no modifica tu copia de trabajo**, solo actualiza el listado de ramas existentes en el remoto.

### 3.2. Lista todas las ramas remotas

```bash
git branch -r
```

Verás ramas del tipo:

```
origin/main
origin/feature-superpoder-luismi
origin/ramita-chill
...
```

---

## 🧳 4. Explora la rama de otra persona

En esta actividad vas a actuar como un explorador que visita el trabajo de otro compañero.

### 4.1. Elige una rama remota interesante

Fíjate en los nombres y elige la que más curiosidad te dé.

### 4.2. Crea una copia local de esa rama

Supongamos que quieres explorar `origin/feature-superpoder-luismi`:

```bash
git switch -c copia-superpoder origin/feature-superpoder-luismi
```

Esto hará dos cosas:

- Crearás una rama local llamada `copia-superpoder`.
- Te situarás en ella con el contenido exacto que existe en el remoto.

### 4.3. Lee lo que ha escrito tu compañero

Abre el archivo modificado en la Actividad 1 (por ejemplo `README.md` o `mensajes.txt`) y busca:

- Su línea absurda
- Su emoji
- Su broma
- Su superpoder secreto

Comenta con tus compañeros lo que encuentres, ¡es parte del juego!

### 4.4. Vuelve a la rama main cuando termines

```bash
git switch main
```

---

## 🎁 5. (Opcional) Explora las ramas sorpresa del profesor

Puede que en el remoto encuentres ramas con nombres como:

- `feature-tesoro`
- `bug-misterioso`
- `mensaje-secreto`
- `reto-ninja`

Puedes explorarlas igual que en el paso anterior.  
Quién sabe qué encontrarás dentro…

---

## 🧠 6. Mini-reflexión

Piensa durante un minuto:

- ¿Qué has tenido que hacer para que tu rama exista en GitHub?
- ¿Qué diferencia ves entre `git fetch` y `git pull`?
- ¿Ha sido difícil crear una rama local a partir de una remota?

---

## 🎉 Resultado final de la actividad

Después de esta actividad habrás aprendido a:

✔ Subir una rama local al remoto usando `git push -u`  
✔ Ver todas las ramas remotas disponibles  
✔ Crear una rama local basada en una rama remota  
✔ Explorar código creado por otras personas  
✔ Entender mejor la diferencia entre **local** y **remoto**

---

¡Actividad completada! Continúa con la siguiente para seguir convirtiéndote en un experto en Git 🚀
