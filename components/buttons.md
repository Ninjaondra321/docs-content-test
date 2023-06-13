# Buttons
Buttons are one of the first things you learn when learning html, so I assume, you already know this. There's nothing to it, just wrap what you want to have inside into button.
## Structure
``` html sample code
<button >Default</button>
<button class="primary">Primary</button>
<button class="secondary">Secondary</button>
<button class="terciary">Tertiary</button>
<button class="plain">Plain</button>
```
## Options
### Link button
You can -of course- use a.btn.primary
``` html sample code
<a href="#" class="btn primary">Primary</a>
<a href="#" class="btn secondary">Secondary</a>
<a href="#" class="btn terciary">Tertiary</a>
<a href="#" class="btn plain">Plain</a>
```
### Large buttons
``` html sample code
<button class="primary "> Hello Word <span class="g-icon">arrow_forward</span></button>
<button class="secondary">Lorem ipsum <span class="g-icon">arrow_forward</span></button>
<button class="terciary">Lorem ipsum <span class="g-icon">arrow_forward</span></button>
<button class="plain">Lorem ipsum <span class="g-icon">arrow_forward</span></button>
```
## Design guidelines
``` css 
a.btn,
a.button,
button,
select {

}

button.primary,
a.btn.primary,
a.button.primary,
select.primary {

}

a.btn.primary:hover,
a.button.primary:hover,
button.primary:hover {

}

button.secondary,
a.btn.secondary,
a.button.secondary,
select.secondary {

}

button.secondary:hover,
a.btn.secondary:hover,
a.button.secondary:hover,
select.secondary:hover {

}
  
button.terciary,
a.btn.terciary,
a.button.terciary,
select.terciary {

}
  
button.terciary:hover,
a.btn.terciary:hover,
a.button.terciary:hover,
select.terciary:hover {

}

button.plain,
a.btn.plain,
a.button.plain,
.icon-btn {

}
  
a.btn.plain:hover,
a.button.plain:hover,
button.plain:hover {

}

button:disabled,
select:disabled {

}

```
