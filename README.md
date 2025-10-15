# Lab4Web
# Praktikum 4: CSS Layout
### NAMA : M. Ridho Febrian
### NIM : 312410500
### KELAS : TI.24.A5

## 📍LANGKAH - LANGKAH PRAKTIKUM

### 1. MEMBUAT DOKUMEN HTML
Persiapan membuat dokumen HTML dengan nama file `lab4_box.html` seperti berikut.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Box Element</title>
  </head>
  <body>
    <header>
      <h1>Box Element</h1>
    </header>
  </body>
</html>
```
### Membuat Box Element
```html
<section>
<div class="div1">Div 1</div>
<div class="div2">Div 2</div>
<div class="div3">Div 3</div>
</section>
```
### CSS Float Property
```css
<style>
div {
float:left;
padding: 10px;
}
.div1 {
background: red;
}
.div2 {
background: yellow;
}
.div3 {
background: green;
}
</style>
```
### Mengatur Clearfix Element
```html
<section>
<div class="div1">Div 1</div>
<div class="div2">Div 2</div>
<div class="div3">Div 3</div>
<div class="div4">Div 4</div>
</section>
```
```css
.div4 {
background-color: blue;
clear: left;
float: none;
}
```
**Tampilan**
<img src="tampilan dan vscode list.png" width="700">
