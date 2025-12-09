# 🌿 Actividad 1 — “Mi Ramillete Personal”
Duración aproximada: 10 minutos  
Objetivo: Aprender a crear, usar y gestionar ramas locales en Git de manera divertida y segura.

---

## 🚀 1. Antes de empezar

En primer lugar debes:

- Tener clonado el repositorio base (o uno que ya estés utilizando).
- Abrir el proyecto en VS Code o en tu editor favorito.
- Comprobar tu estado actual ejecutando:

```bash
git status
```

Asegúrate de estar en la rama `main` y sin cambios pendientes.

---

## 🌱 2. Crea tu propia rama creativa

Ahora vas a crear una rama donde podrás trabajar sin afectar al resto del proyecto.

1. Elige un nombre divertido o extraño para tu rama. Algunas ideas por si necesitas inspiración:

   - `feature-superpoder-luismi`
   - `fix-unicornio-rabioso`
   - `ramita-chill`
   - `idea-misteriosa-42`
   - `experimento-kiwi`

2. Crea tu rama con el comando:

```bash
git switch -c nombre-de-tu-rama
```

3. Comprueba que te has cambiado correctamente:

```bash
git branch
```

La rama marcada con `*` es en la que te encuentras ahora.

---

## ✏️ 3. Añade tu aporte divertido al proyecto

Vas a hacer una pequeña modificación para experimentar con esta nueva rama.

1. Abre el archivo indicado por el profesor (por ejemplo `README.md` o `mensajes.txt`).
2. Añade una línea creativa, absurda o graciosa. Algunas ideas:

   - “🦄 Mi poder secreto es debuggear sin mirar la pantalla.”
   - “✨ Consejo de vida: programa con estilo.”
   - “🐙 Git tiene tentáculos y cada commit es uno nuevo.”
   - “🚀 Hoy he creado más ramas que un árbol de Navidad.”

3. Guarda los cambios y súbelos al *stage*:

```bash
git add .
```

4. Haz un commit:

```bash
git commit -m "Añadiendo mi superpoder secreto ✨"
```

---

## 🔄 4. Vuelve a la rama main

Para comprobar cómo funciona el aislamiento de ramas en Git, vuelve a `main`:

```bash
git switch main
```

Si ahora abres el archivo que modificaste, verás que **tu línea divertida no está ahí**.  
Esto es porque tus cambios viven únicamente en tu rama personal.

---

## 🔍 5. (Opcional) Comprueba la diferencia entre tu rama y main

Si quieres ver la diferencia exacta entre lo que has cambiado y lo que hay en `main`:

```bash
git diff nombre-de-tu-rama
```

Así podrás visualizar qué aporta tu rama al proyecto.

---

## 🧠 6. Mini-reflexión

Piensa brevemente:

- ¿Has roto algo en `main` al hacer tus cambios?  
- ¿Qué tan rápido has podido crear tu rama?  
- ¿Te ha resultado más seguro trabajar en tu propia rama que modificar `main`?

La respuesta debería ser **sí**: trabajar con ramas te permite experimentar sin miedo.

---

## 🎉 Resultado final de la actividad

Al terminar esta actividad habrás logrado:

✔ Crear una rama local en Git  
✔ Realizar cambios aislados del resto del proyecto  
✔ Registrar tus cambios con un commit  
✔ Alternar entre ramas  
✔ Entender por qué las ramas hacen el trabajo más seguro y ordenado  
