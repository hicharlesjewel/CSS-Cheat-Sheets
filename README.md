# **CSS-Cheat-Sheets**

Hojas de trucos para aprender CSS.

---

## **Añadir CSS a HTML**

---

### **Enlace externo**

> Colocar el CSS en un archivo externo y enlazarlo con el HTML.

```html
<link rel="stylesheet" href="style.css" />
```

---

## **Comentarios**

---

```css
/* Comentario de una línea */
```

```css
/*
Comentario de varias líneas
*/
```

---

## **Selectores**

---

> Los selectores es la primera parte de una regla CSS. Definen que elementos del html serán modificados, todos los elementos del html que coincidan con el selector serán modificados.

---

### **Basico**

---

#### **Universal**

> Selecciona todos los elementos.

```css
* {
  color: red;
}
```

---

#### **Etiqueta**

> Selecciona todos los elementos que tengan la etiqueta.

```css
h1 {
  color: red;
}
```

```html
<h1>Hola</h1>
```

---

#### **Clase**

> Selecciona todos los elementos que tengan la clase.

```css
.clase {
  color: red;
}
```

```html
<p class="clase">Hola</p>
```

---

#### **ID**

> Selecciona el elemento que tenga el ID.

```css
#id {
  color: red;
}
```

```html
<p id="id">Hola</p>
```

---

### **Combinadores**

---

#### **Descendiente**

> Selecciona a los descendientes de un elemento.

```css
.lista li {
  color: red;
}
```

```html
<ul class="lista">
  <!-- Descendiente -->
  <li>Hola</li>
  <!-- Descendiente -->
  <li class="elemento">Hola</li>
  <!-- Descendiente -->
  <li>Hola</li>
  <ul>
    <!-- Descendiente -->
    <li>Hola</li>
    <!-- Descendiente -->
    <li>Hola</li>
    <!-- Descendiente -->
    <li>Hola</li>
  </ul>
  <!-- Descendiente -->
  <li>Hola</li>
</ul>
```

---

#### **Hijo**

> Selecciona todos los elementos que sean hijos directos de otro elemento.

```css
.lista > li {
  color: red;
}
```

```html
<ul class="lista">
  <!-- Hijo -->
  <li>Hola</li>
  <!-- Hijo -->
  <li class="elemento">Hola</li>
  <!-- Hijo -->
  <li>Hola</li>
  <ul>
    <li>Hola</li>
    <li>Hola</li>
    <li>Hola</li>
  </ul>
  <!-- Hijo -->
  <li>Hola</li>
</ul>
```

---

#### **Hermano adyacente**

> Selecciona todos los elementos que sean hermanos de otro elemento.

```css
.elemento + li {
  color: red;
}
```

```html
<ul class="lista">
  <li>Hola</li>
  <li class="elemento">Hola</li>
  <!-- Hermano adyacente -->
  <li>Hola</li>
  <ul>
    <li>Hola</li>
    <li>Hola</li>
    <li>Hola</li>
  </ul>
  <li>Hola</li>
</ul>
```

---

#### **Hermano siguiente**

> Selecciona todos los elementos que sean hermanos directos de otro elemento.

```css
.elemento ~ li {
  color: red;
}
```

```html
<ul class="lista">
  <li>Hola</li>
  <li class="elemento">Hola</li>
  <!-- Hermano siguiente -->
  <li>Hola</li>
  <ul>
    <li>Hola</li>
    <li>Hola</li>
    <li>Hola</li>
  </ul>
  <!-- Hermano siguiente -->
  <li>Hola</li>
</ul>
```

---

### **Atributos**

---

#### **Atributo**

> Selecciona todos los elementos que tengan el atributo.

```css
[type] {
  background-color: yellow;
}
```

```html
<h2 class="title">Titulo</h2>
<form class="form">
  <!-- Atributo -->
  <input type="text" value="This is text area." />
  <!-- Atributo -->
  <input type="password" value="This is a password." />
  <!-- Atributo -->
  <input type="email" value="This is a email area." />
  <!-- Atributo -->
  <input type="submit" value="Eject button" />
</form>
```

---

#### **Atributo con valor exacto**

> Selecciona todos los elementos que tengan el atributo con el valor exacto especificado.

```css
[type="text"] {
  background-color: yellow;
}
```

```html
<h2 class="title">Titulo</h2>
<form class="form">
  <!-- Atributo exacto -->
  <input type="text" value="This is text area." />
  <input type="password" value="This is a password." />
  <input type="email" value="This is a email area." />
  <input type="submit" value="Eject button" />
</form>
```

---

#### **Atributo con valor parcial**

> Selecciona todos los elementos que tengan el atributo con el valor parcial especificado.

```css
[value*="is a"] {
  background-color: yellow;
}
```

```html
<h2 class="title">Titulo</h2>
<form class="form">
  <input type="text" value="This is text area." />
  <!-- Atributo parcial -->
  <input type="password" value="This is a password." />
  <!-- Atributo parcial -->
  <input type="email" value="This is a email area." />
  <input type="submit" value="Eject button" />
</form>
```

---

#### **Atributo con valor de inicio**

> Selecciona todos los elementos que tengan el atributo con el valor de inicio especificado.

```css
[value^="This"] {
  background-color: yellow;
}
```

```html
<h2 class="title">Titulo</h2>
<form class="form">
  <!-- Atributo inicio -->
  <input type="text" value="This is text area." />
  <!-- Atributo inicio -->
  <input type="password" value="This is a password." />
  <!-- Atributo inicio -->
  <input type="email" value="This is a email area." />
  <input type="submit" value="Eject button" />
</form>
```

---

#### **Atributo con valor de final**

> Selecciona todos los elementos que tengan el atributo con el valor de final especificado.

```css
[value$="area."] {
  background-color: yellow;
}
```

```html
<h2 class="title">Titulo</h2>
<form class="form">
  <!-- Atributo final -->
  <input type="text" value="This is text area." />
  <input type="password" value="This is a password." />
  <!-- Atributo final -->
  <input type="email" value="This is a email area." />
  <input type="submit" value="Eject button" />
</form>
```

---

#### **Atributo con valor de separación**

> Selecciona todos los elementos que tengan el atributo con el valor de separación especificado.

```css
[value~="is"] {
  background-color: yellow;
}
```

```html
<h2 class="title">Titulo</h2>
<form class="form">
  <!-- Atributo separación -->
  <input type="text" value="This is text area." />
  <!-- Atributo separación -->
  <input type="password" value="This is a password." />
  <!-- Atributo separación -->
  <input type="email" value="This is a email area." />
  <input type="submit" value="Eject button" />
</form>
```

---

#### **Atributo con valor de lista**

> Selecciona todos los elementos que tengan el atributo con el valor de lista especificado.

```css
[value|="is"] {
  background-color: yellow;
}
```

```html
<h2 class="title">Titulo</h2>
<form class="form">
  <!-- Atributo lista -->
  <input type="text" value="This is text area." />
  <!-- Atributo lista -->
  <input type="password" value="This is a password." />
  <!-- Atributo lista -->
  <input type="email" value="This is a email area." />
  <input type="submit" value="Eject button" />
</form>
```

---

## **Herencia**

> La herencia es la capacidad de un elemento de heredar propiedades de sus elementos padres.

---

## **Especificidad**

> La especificidad es la capacidad de un elemento de sobreescribir propiedades de sus elementos heredados. Entre mas grande sea la especificidad, mas prioridad tendrá el elemento.

```css
/* Especificidad 0,0,1 */
/* Tipo */
h1 {
  color: red;
  font-size: 30px;
}
/* Especificidad 0,1,0 */
/* Clase */
.title {
  color: blue;
  font-size: 20px;
}
/* Especificidad 1,0,0 */
/* ID */
#title {
  color: purple;
  font-size: 20px;
}
/* Especificidad 0,1,1 */
h1.title {
  color: green;
  font-size: 20px;
}
```

---

## **Cascada**

> La cascada es la capacidad de un elemento de sobreescribir propiedades de sus elementos heredados y especificados.

```css
h1 {
  color: red;
  font-size: 30px;
}
h1 {
  color: blue;
  /* Cascada */
  font-size: 20px;
}
h1 {
  color: purple;
  /* Cascada */
  color: green;
}
```

---

## **BEM**

> BEM es un método de nomenclatura para clases y selectores en CSS.

```css

```
