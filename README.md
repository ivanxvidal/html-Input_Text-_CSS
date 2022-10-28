# Estilos de input="text" con CSS

Utilizando:

- Html
- Css

## Input Type="Text" Simple

Dentro de la etiqueta `<style>` se escribe lo siguiente:

```Css
.input__simple {
    border: none;
    -webkit-appearance: none;
    -ms-progress-appearance: none;
    -moz-appearance: none;
    appearance: none;
    background: #f2f2f2;
    padding: 12px;
    border-radius: 3px;
    width: 250px;
    outline: none;
}
```

Para el `<html>` es:

```html
<input type="text" class="input__simple" placeholder="Entrada de datos" />
```

Teniendo como resultado:

![input_simple](/Input_Text%20_CSS/img/input_simple.png)

## Input Type="Text" con placeholder Flotante

Dentro de la etiqueta `<style>` se escribe lo siguiente:

```Css
.input__flotante {
    position: relative;
}
.input__flotante > input {
    border: none;
    -webkit-appearance: none;
    -ms-progress-appearance: none;
    -moz-appearance: none;
    appearance: none;
    background: #f2f2f2;
    padding: 12px;
    border-radius: 3px;
    width: 250px;
    outline: none;
}
.input__flotante .placeholder {
    position: absolute;
    left: 12px;
    top: calc(50%);
    transform: translateY(-50%);
    color: #aaa;
    transition: top 0.3s ease, font-size 0.3s ease, color 0.3s  ease;
}
.input__flotante input:focus + .placeholder,
.input__flotante input:valid + .placeholder {
    top: -10px;
    font-size: 12px;
    color: #222;
}
```

Para el `<html>` es:

```html
<label class="input__flotante">
  <input type="text" required />
  <span class="placeholder">Entrada de datos</span>
</label>
```

Teniendo como resultado:

![input_flotante](/Input_Text%20_CSS/img/input_flotante.PNG)

## Input Type="Text" con Contorno

Dentro de la etiqueta `<style>` se escribe lo siguiente:

```Css
.input__contorno {
    position: relative;
}
.input__contorno > input {
    border: none;
    -webkit-appearance: none;
    -ms-progress-appearance: none;
    -moz-appearance: none;
    appearance: none;
    background: none;
    padding: 12px;
    border-radius: 3px;
    border: 2px solid #ddd;
    width: 250px;
    outline: none;
    transition: border 0.3s ease;
}
.input__contorno > input:focus,
.input__contorno > input:valid {
    border: 2px solid #222;
}
.input__contorno .placeholder {
    position: absolute;
    left: 10px;
    top: calc(50%);
    transform: translateY(-50%);
    color: #aaa;
    transition: all 0.3s ease-in-out;
}
.input__contorno input:focus + .placeholder,
.input__contorno input:valid + .placeholder {
    top: 0px;
    font-size: 12px;
    color: #222;
    background: #fff;
    padding: 0 5px;
}
```

Para el `<html>` es:

```html
<label class="input__contorno">
  <input type="text" required />
  <span class="placeholder">Entrada de datos</span>
</label>
```

Teniendo como resultado:

![input_contorno](/Input_Text%20_CSS/img/input_contorno.PNG)

## Input Type="Text" con Linea debajo

Dentro de la etiqueta `<style>` se escribe lo siguiente:

```Css
.input__linea {
    position: relative;
}
.input__linea > input {
    border: none;
    -webkit-appearance: none;
    -ms-progress-appearance: none;
    -moz-appearance: none;
    appearance: none;
    background: linear-gradient(90deg, #222, #222) center bottom/0 2px no-repeat,
        linear-gradient(90deg, #ccc, #ccc) left bottom/100% 2px no-repeat,
        linear-gradient(90deg, #fafafa, #fafafa) left bottom/100% no-repeat;
    padding: 12px;
    border-radius: 3px;
    width: 250px;
    outline: none;
    transition: background-size 0.3s ease;
}
.input__linea > input:focus,
.input__linea > input:valid {
    background-size: 100% 2px, 100% 2px, 100%;
}
.input__linea .placeholder {
    position: absolute;
    left: 8px;
    top: calc(50%);
    color: #aaa;
    transform: translateY(-50%);
    transition: top 0.3s ease, font-size 0.3s ease, color 0.3s ease;
}
.input__linea input:focus + .placeholder,
.input__linea input:valid + .placeholder {
    top: -10px;
    font-size: 12px;
    color: #222;
}
```

Para el `<html>` es:

```html
<label class="input__linea">
  <input type="text" required class="cuarto" />
  <span class="placeholder">Entrada de datos</span>
</label>
```

Teniendo como resultado:

![input_linea](/Input_Text%20_CSS/img/input_linea.PNG)
