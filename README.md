# actividad-branchingof
---
# 1 Diego Castillo.
# 🌿 ¿Qué es una rama en Git?

## 📌 Definición
- **Qué es una branch:**  
  Una rama (*branch*) en Git es una copia independiente del código donde puedes trabajar sin afectar la versión principal del proyecto.

## 🎯 ¿Para qué sirve?
- Permiten separar tareas sin mezclar todo el trabajo.

## ⚠️ ¿Qué problema resuelve?
- Evitan romper el código principal mientras se desarrollan nuevas funcionalidades.

## 🚫 ¿Por qué no trabajar siempre en `main`?
- Porque la rama `main` debe mantenerse estable y sin errores.

---

## 💡 Ejemplo

Estás desarrollando una página web en Git.  
Tienes la rama `main` funcionando correctamente, pero necesitas agregar un login.

En lugar de trabajar directamente en `main`:

- Creas una rama llamada `login`
- Desarrollas el login ahí
- Si hay errores, no afectan el proyecto principal
- Cuando todo funciona bien, unes la rama a `main`

---
...


## ✅ Conclusión



Las ramas son fundamentales porque permiten trabajar de forma ordenada y segura, evitando errores en el código principal y facilitando el desarrollo en equipo.

---





# Respuesta-Alumno-DiegoContreras

1. ¿Que es un merge?

 El merge en github es la fusión de ramas que generalmente es la rama main para poder incorporar el código nuevo al proyecto.

2. ¿Qué es un conflicto de merge?

 Esto ocurre cuando se editaron en la misma linea de código del mismo archivo de formas distintas. 
 Pensandolo como programador: El programador (Diego) edito código en la linea 20 de un archivo html y el programador (David)    hizo modificaciones en la misma linea, en este punto git se detiene y va a decir: "cúal versión debo guardar?, la de Diego o   David, eso lo decides tú"

3. ¿Cómo puede evitarse o reducirse?

   1. Comunicación con el equipo
      Avisar antes de trabajar en un archivo o feature. Un simple mensaje en el canal del equipo evita que dos personas toquen        lo mismo al mismo tiempo.
      
   2. Trabajar en ramas pequeñas y cortas
      Mientras más tiempo viva una rama sin mergearse, más probabilidad de conflicto. Lo ideal es hacer ramas enfocadas en una        sola tarea y mergearlas rápido.

   3. Hacer pull frecuente
      Antes de empezar a trabajar y durante el desarrollo, traer los últimos cambios del repositorio:
      bashgit pull origin main
      Así tu rama siempre está actualizada con lo que hicieron los demás.

   4. Dividir bien el trabajo
      Cada persona trabaja en archivos o módulos distintos. Si el equipo tiene clara la separación de responsabilidades, los          conflictos bajan mucho.
   
---

## Trabajo de Kevin Lizama

1. Branch vs. Fork: Gestión de Flujos de Trabajo
En el ecosistema de Git y plataformas como GitHub, la diferencia fundamental entre estos conceptos radica en el alcance (scope) y la propiedad (ownership) del repositorio.

¿Qué es una Branch (Rama)?
Es una línea de desarrollo separada dentro del mismo repositorio. Técnicamente, una rama es un puntero móvil que apunta a un commit específico. Permite desarrollar funcionalidades o corregir errores de forma aislada, sin afectar la línea principal (main o master) hasta que los cambios sean validados.

¿Qué es un Fork?
Un Fork no es un comando nativo de Git, sino una funcionalidad de plataformas de hosting (como GitHub). Es una copia completa y remota de un repositorio que se aloja en la cuenta personal del usuario. A diferencia de la rama, el fork genera un repositorio independiente con su propio historial y permisos de acceso específicos.

Cuándo se usa cada uno
Branch: Se utiliza para el desarrollo diario dentro de un equipo que posee permisos de escritura en el repositorio. Es el componente esencial del modelo de Feature Branching.

Fork: Se utiliza principalmente en proyectos de Open Source o cuando se desea contribuir a un proyecto donde no se tienen permisos directos de colaboración. Permite experimentar libremente sin riesgo de alterar el proyecto original.

Por qué GitHub usa forks para contribuir a proyectos ajenos
El uso de forks responde a un principio de seguridad y control de acceso (conocido como Principio de Menor Privilegio). Dado que un colaborador externo no es dueño del repositorio original (upstream), no posee permisos para realizar un push directamente.

El flujo de trabajo estándar bajo este modelo es:

Realizar un Fork: El colaborador obtiene su propia copia del proyecto.

Desarrollo Local: Se trabaja en la copia personal (fork).

Pull Request (PR): Se envían los cambios desde el fork hacia el repositorio original para que el administrador los revise, comente y, finalmente, realice el merge si cumplen con los estándares de calidad.