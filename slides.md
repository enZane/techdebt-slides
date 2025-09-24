---
theme: neversink
title: Technical Debt
color: pink
info: |
  ## Technical Debt
  A presentation about managing and understanding technical debt in software development.
class: text-center
transition: slide-left
mdc: true
---

# Deuda técnica

Pagar después para avanzar hoy

---
layout: center
---


<div class="grid grid-cols-3">
  <div class="col-span-2">
    <Browser mood="ko" :size="350" color="#2fdbe4ff" />
  </div>

<div>

# ¿Qué es la deuda técnica?

Es cuando haces algo rápido que sabes que después va a alentarte.

<br>

Hacer una mexicanada (hack) para salir del problema.

<br>

Un castigo a mi yo del futuro.
</div>
</div>

---
layout: quote
author: Ward Cunningham
---
Shipping first time code is like going into debt.
---
layout: fact
class: text-white bg-orange
---

# La Deuda Técnica es buena.


---
layout: center
---


<div class="grid grid-cols-3 grid-cols-reverse">
  <div class="col-span-2">
    <Browser mood="happy" :size="350" color="#2fdbe4ff" />
  </div>

<div>

# Es una decisión estratégica

- Te permite avanzar rápido

- Da flexibilidad para el feedback rápido

- Puedes corregir decisiones de diseño

</div>
</div>

---
layout: fact
color: pink
---

# Es una señal de que estás aprendiendo

---
layout: center
---

# El Cuadrante de Deuda Técnica

<div class="relative mt-20">
  <!-- Axis Labels -->
  <div class="absolute top-0 left-1/2 transform -translate-x-1/2 -translate-y-8">
    <p class="text-lg font-bold">Deliberada</p>
  </div>
  <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 translate-y-8">
    <p class="text-lg font-bold">Accidental</p>
  </div>
  <div class="absolute left-0 top-1/2 transform -translate-y-1/2 -translate-x-16 -rotate-90">
    <p class="text-lg font-bold">Imprudente</p>
  </div>
  <div class="absolute right-0 top-1/2 transform -translate-y-1/2 translate-x-16 rotate-90">
    <p class="text-lg font-bold">Prudente</p>
  </div>

  <!-- Chart with borders -->
  <div class="grid grid-cols-2 border-2 border-gray-400">
    <div class="text-center border-r border-b border-gray-400 bg-red-100 p-6">
      <Browser mood="ko" :size="80" color="#ef4444" />
      <p class="text-sm font-bold mt-2">"No tenemos tiempo para diseño"</p>
    </div>
    <div class="text-center border-b border-gray-400 bg-green-100 p-6">
      <Browser mood="happy" :size="80" color="#22c55e" />
      <p class="text-sm font-bold mt-2">"Debemos avanzar ahora y lidiar con las consecuencias"</p>
    </div>
    <div class="text-center border-r border-gray-400 bg-purple-100 p-6">
      <Cat mood="shocked" :size="80" color="#a855f7" />
      <p class="text-sm font-bold mt-2">"Como qué arquitectura?"</p>
    </div>
    <div class="text-center bg-blue-100 p-6">
      <IceCream mood="happy" :size="80" color="#3b82f6" />
      <p class="text-sm font-bold mt-2">"Ahora sabemos cómo hacerlo"</p>
    </div>
  </div>
</div>

---
layout: quote
---

Many have explained the debt metaphor and confused it with the idea that you could write code poorly with the intention of doing a good job later.

---
layout: fact
---

<h2>
El pagar la deuda técnica depende de que el código escrito sea lo <span class="text-blue">suficientemente bueno</span> para permitir un refactor tan pronto como entiendes el problema
</h2>

---
layout: side-title
---

::title::

<SpeechBubble color="pink-light" class="text-left" position="bl" shape="round" animation="float">

## ¿Tengo deuda técnica?

</SpeechBubble>

<div class="flex justify-center mt-8">
  <Cat mood="happy" :size="250" color="#fccb77ff" />
</div>

::content::

<div class="flex flex-col gap-4">
  <Admonition  color="blue-light" textAlign="left"  title="Aprendizaje" class="">

📚 Hay oportunidad de **aprendizaje**

  </Admonition>

  <Admonition color="green-light" textAlign="left"  title="Plan" class=" ">

💰 Hay un plan para **pagar**

</Admonition>

  <Admonition color="yellow-light" textAlign="left"  title="Negocio"  class=" ">

🏢 Tenemos la suficiente información del **negocio**
  </Admonition>

  <Admonition color="pink-light" textAlign="left"  title="Limpio">

✨ El código es **limpio**

  </Admonition>

  <Admonition color="purple-light" textAlign="left"  title="Tests" >

🧪 El código tiene **tests**

  </Admonition>
</div>

---

<AIQATool />

---
layout: section
color: black
---

# LOCK IN AND SHIP