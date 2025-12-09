# 🔥 Actividad 3 — “Resolver el Caos”
### Duración aproximada: 15 minutos  
### Objetivo: Aprender a resolver conflictos de fusión (merge conflicts) en Git de forma controlada y sin miedo.

---

# 🧠 1. ¿Qué vas a aprender en esta actividad?

En esta actividad vas a:

- Provocar un conflicto de fusión en Git (de forma segura).  
- Ver cómo Git marca las partes que chocan (`<<<<<<<`, `=======`, `>>>>>>>`).  
- Editar el archivo para resolver el conflicto manualmente.  
- Completar el merge y dejar el repositorio en un estado correcto.

Los conflictos son algo **normal** cuando varias personas modifican las mismas líneas de un archivo. ¡No son errores! Son oportunidades de colaboración.

---

# 🚀 2. Preparación inicial

Antes de comenzar, asegúrate de:

- Tener un repositorio clonado y funcionando.
- Haber completado las actividades 1 y 2.
- Estar en la rama `main`:

```bash
git switch main
git pull
```

Tu profesor ya debe haber preparado una situación donde **dos ramas modifican la misma línea de un archivo**, lo que garantizará que aparece un conflicto.

---

# 🌱 3. Crea una rama para provocar el conflicto

1. Crea una rama llamada, por ejemplo:

```bash
git switch -c mi-conflicto
```

2. Abre el archivo indicado por el profesor (normalmente `README.md` o `mensajes.txt`).

3. Busca la sección o línea que te indique el profesor.  
   Modifícala de forma sencilla, por ejemplo:

```
Esta es mi versión de la línea conflictiva 😼
```

4. Guarda los cambios y haz commit:

```bash
git add .
git commit -m "Mi versión de la línea conflictiva"
```

---

# 🔀 4. Intenta fusionar tu rama con main (y observa el conflicto)

Ahora vuelve a `main`:

```bash
git switch main
```

Y trata de fusionar tu rama:

```bash
git merge mi-conflicto
```

Git mostrará un mensaje parecido a:

```
CONFLICT (content): Merge conflict in mensajes.txt
Automatic merge failed; fix conflicts and then commit the result.
```

🎉 ¡Acabas de generar un conflicto!

---

# 🧩 5. Entendiendo un conflicto de merge

Abre el archivo con conflicto. Verás algo como:

```
<<<<<<< HEAD
Versión que estaba en main
=======
Esta es mi versión de la línea conflictiva 😼
>>>>>>> mi-conflicto
```

Significa:

- `<<<<<<< HEAD` → lo que existe en `main`
- `=======`       → separación entre versiones
- `>>>>>>> mi-conflicto` → lo que viene de tu rama

---

# 🛠️ 6. Resuelve el conflicto

Tu tarea es **editar el archivo manualmente** para dejar una versión final coherente.  
Ejemplo:

```
Esta es la versión final, combinando ideas 😼✨
```

Luego elimina completamente las marcas:

- `<<<<<<<`
- `=======`
- `>>>>>>>`

Guarda el archivo.

---

# 💾 7. Marca el conflicto como resuelto

Cuando hayas terminado:

```bash
git add .
git commit -m "Resolviendo conflicto de merge"
```

Si quieres comprobar el estado antes:

```bash
git status
```

---

# ⭐ 8. Verifica que todo está correcto

Comprueba que el merge se completó:

```bash
git log --oneline --graph --decorate --all
```

Opcionalmente, puedes abrir el archivo afectado y verificar que se quedó la versión final que tú escribiste.

---

# 🎉 9. Resultado final de la actividad

Después de esta actividad habrás aprendido:

✔ Qué es un conflicto de merge  
✔ Por qué ocurren (y por qué no son errores graves)  
✔ Cómo identificarlos en un archivo  
✔ Cómo resolverlos editando el contenido  
✔ Cómo completar correctamente un merge después de resolver el conflicto  

---

¡Enhorabuena! Has superado uno de los mayores miedos de los programadores novatos 🎉  
Ya estás listo para trabajar con ramas en equipos reales 🚀
