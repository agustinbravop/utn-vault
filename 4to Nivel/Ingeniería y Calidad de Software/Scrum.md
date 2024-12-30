Es un **framework iterativo-incremental para la gestión de proyectos** de software. Hoy en día se trata de aplicar a más áreas, no solo a la [[Ingeniería de Software]]. Creado por Ken Schwaber y Jeff Sutherland, es parte de la [[Agilidad]]. Scrum gestiona **personas**, **necesidades** y **tiempo**.

La **guía 2020** dice que cada práctica sugerida debe ser evaluada antes de implementarse, por lo que Scrum trata de **sugerir** y no imponer.

![[Proceso de Scrum.png]]

Scrum es muy utilizado en la **industria**, pero no siempre se sigue la guía scrum al pie de la letra:

- A veces no hay Scrum Master y uno del equipo de desarrollo rellena ese rol.
- No suele haber un representante del cliente disponible 24/7, y se utiliza un "Business Analyst".
- A veces puede haber muchos POs y no se sabe a quién hacerle caso.
- Se puede hacer una **_weekly_** en lugar de una _daily_.

## 5 Valores

1. **Compromiso**
2. **Coraje**
3. **Apertura** (a opiniones, alternativas de decisión y solución)
4. **Enfoque** (al objetivo del proyecto)
5. **Respeto**

## 3 Pilares

1. **Transparencia**: todo miembro del equipo puede **conocer el avance actual** del proyecto. Se usan **tableros** entendibles por todos y **reuniones** que sincronicen al equipo.
2. **Inspección**: en cualquier momento podemos **evaluar** cómo estamos trabajando, desde el punto de vista **técnico** y del **proceso**.
3. **Adaptación**: le damos la **bienvenida a los cambios** para **corregir** lo que funciona mal.

## 3 Artefactos

1. **[[Product Backlog]]**: con el compromiso del **Product Goal**.
2. **Sprint Backlog**: con el compromiso del **Sprint Goal**.
3. **Increment**: con el compromiso del [[Definition of Done]].

## Roles

Scrum define una serie de roles para gestionar las **personas** **responsables** del proyecto:

- **Primarios**: es el **equipo scrum** **comprometido** (compromiso equitativo) a lograr los objetivos.
  1.  **Equipo de Desarrollo**: es el [[Equipo Ágil]] que **lleva a cabo** el proyecto. Aseguran la **calidad** al construir correctamente.
  2.  **Scrum Master**: es el **facilitador** del **proceso** de Scrum. Ayuda a construir de **manera** correcta respetando Scrum.
  3.  **Product Owner**: define el **alcance** (qué hacemos y qué no hacemos). Nos permite construir lo correcto para satisfacer las **necesidades**.
- **Secundarios**: solo están **involucrados** en el proyecto. Son los _stakeholders_ y los usuarios.

## Necesidades

Las necesidades son un conjunto de ítems ([[4to Nivel/Ingeniería y Calidad de Software/Historias de Usuario|Historias de Usuario]] que cumplan el método _INVEST_) ordenados por prioridad según el PO y organizados en el [[Product Backlog]], el cual está en constante movimiento. Cuando llegan nuevas HUs cambian las prioridades existentes. El SM puede ayudar al PO a organizar el backlog.

## Ceremonias

Scrum define un conjunto de ceremonias alrededor de cada [[Sprint]], los cuales duran entre 1 y 4 semanas.

### Sprint Planning

Se reúnen el equipo scrum (PO + SM + devs) para hacer la [[Estimación]] y definir el **sprint backlog**: el conjunto de HUs que serán el objetivo del sprint. Se debate, negocia, entiende, y reajusta todo.

### Daily

**Todos los días** de trabajo se reúne brevemente el equipo para **actualizar el tablero**:

- Reunión de **15 minutos** máximo al **inicio** de la jornada laboral.
- **Todos se paran** para incomodarse y terminar rápido.
- Cada uno comparte **avances y problemas** (después se pueden solucionar los **bloqueos**).
- El SM debe asegurarse que sea **corta y enfocada**.
- Permite **detectar atrasos**.
- **Sincroniza** al equipo para que todos sepan lo que está haciendo el resto.

### Sprint Review

**Al final del sprint se le muestra al PO el working software** logrado. Se ve el estado de cada HU y se muestran solo las _done_. Participa el equipo scrum entero. El **PO valida cada HU** y vuelven al backlog las insatisfactorias. No necesariamente implica un pase a producción o release.

### Sprint Retrospective

**Evaluación frecuente del proceso** (no del producto) del equipo que se hace cada X cantidad de sprints o cuando algo grave sucedió. Participa el equipo scrum para charlar sobre lo que se hizo bien y mal en la **forma de trabajar**. Es importante definir **accionables** para mejorar a corto y largo plazo.

Hay muchas técnicas para la retrospectiva. Algunas son:

- La estrella de mar.
- El bote.
- Las 4 Ls.

## Beneficios

- **Entrega periódica** de resultados.
- **Entregas parciales** (se limitan riesgos y costos).
- **Flexibilidad** y **adaptación** a las necesidades (cambiantes) del cliente.
- **Mejores estimaciones**.
