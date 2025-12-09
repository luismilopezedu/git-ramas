# 🏰 Actividad 4 — “Carrera del Merge”
### Duración aproximada: 10–12 minutos  
### Objetivo: Practicar la integración de varias ramas en una sola rama de equipo, simulando un entorno real de colaboración.

---

# 🧠 1. ¿Qué vas a hacer en esta actividad?

En esta actividad trabajarás en equipo para:

- Integrar **varias ramas** en una rama de integración.
- Evitar merges innecesarios.
- Resolver posibles conflictos.
- Mantener un historial ordenado y limpio.
- Aprender a colaborar como en un proyecto real.

El reto está gamificado: ¡tu equipo competirá con otros para ver quién realiza la integración más clara, ordenada y rápida!

---

# 👥 2. Organización por equipos

Forma equipos de **3 o 4 personas**.

Cada equipo tendrá acceso a **tres ramas creadas previamente por el profesor**, por ejemplo:

- `feature-torre`
- `feature-muralla`
- `feature-puerta`

(El nombre puede variar según la temática del profesor.)

Tu misión será fusionarlas todas en una rama final, por ejemplo:

```
castillo-final
```

o cualquier nombre que os indique vuestro profesor.

---

# 🚀 3. Crea la rama de integración del equipo

Primero, sitúate en `main`:

```bash
git switch main
git pull
```

Luego crea y cambia a vuestra rama de integración:

```bash
git switch -c castillo-final
```

(Los equipos pueden elegir otro nombre, siempre que sea coherente.)

---

# 🔀 4. Integra las ramas una a una

Ahora llega la parte importante: **fusionar las ramas del profesor dentro de vuestra rama de integración**.

La secuencia habitual es:

```bash
git merge feature-torre
git merge feature-muralla
git merge feature-puerta
```

Puedes fusionarlas en cualquier orden, pero te recomendamos:

1. Fusionar primero la que parezca más sencilla.  
2. Guardar para el final la que podría generar conflictos.

Durante esta fase puede que Git muestre mensajes como:

```
Already up to date.
Merge made by the 'ort' strategy.
CONFLICT (content): Merge conflict in archivo.txt
```

Si ocurre un conflicto:

1. Abre el archivo afectado.  
2. Resuélvelo como aprendiste en la **Actividad 3**.  
3. Guarda el archivo.  
4. Registra la resolución:

```bash
git add .
git commit -m "Resolviendo conflicto al integrar feature-muralla"
```

---

# 🧹 5. Mantén el historial limpio

Cuando termines todas las fusiones, revisa tu historial con:

```bash
git log --oneline --graph --decorate --all
```

Deberías ver algo como:

```
*   Merge branch 'feature-puerta'
|| * Nueva funcionalidad puerta
* | Integración de feature-muralla
|/
* Integración de feature-torre
* Rama 'main' actualizada
```

Tu objetivo es que el historial sea **claro**, **legible** y sin merges duplicados.

---

# 📝 6. Escribe un mensaje final claro

Una vez integradas todas las ramas, añade un commit final opcional para dejar constancia del resultado:

```bash
git commit --allow-empty -m "Integración final del castillo completada 🏰"
```

Esto crea un punto de referencia en el historial.

---

# 🧪 7. Comprueba que todo funciona

Según el proyecto usado, revisa:

- Archivos modificados
- Coherencia del contenido final
- Ausencia de marcas de conflicto (`<<<<<<<`, `=======`, `>>>>>>>`)
- Ejecución correcta del programa *(si aplica)*

---

# 🏆 8. Cierre del reto

Comparad con otros equipos:

- ¿Quién ha terminado primero?
- ¿Quién ha mantenido el historial más limpio?
- ¿Qué equipos han tenido conflictos?
- ¿Cómo los habéis resuelto?

Este ejercicio imita lo que ocurre en proyectos colaborativos reales.

---

# 🎉 Resultado final de la actividad

Después de esta actividad habrás aprendido a:

✔ Integrar varias ramas en una sola  
✔ Resolver conflictos dentro de merges complejos  
✔ Mantener un historial legible  
✔ Trabajar en equipo usando Git  
✔ Prepararte para flujos de trabajo tipo Git Flow, GitHub Flow, etc.

---

¡Enhorabuena! Has completado la última actividad práctica del módulo de ramificación 🚀  
Ahora estás mucho más preparado para trabajar con Git en proyectos reales.
