# Inputs
Inputs are key element in every website. With BESAMEL, inputs have fixed structure, so it may seem complicated at first, but it's all for a reason.
``` html sample
<div className="input">
  <label htmlFor="theID">Input</label>
  <input type="text" name="Hello" id="theID" placeholder="Hovno v koši" />
  <label htmlFor="theID" class="sub">Heslo musí obsahovat alespoň jednu číslici</label>
  <label htmlFor="theID" class="sub">Heslo musí obsahovat alespoň sedmncáct trpaslíků</label>
</div>
````
## Structure
``` html
<div className="input">
  <label htmlFor="theID">Input</label>
  <input type="text" name="Hello" id="theID" placeholder="Hovno v koši" />
  <label htmlFor="theID" class="sub">Heslo musí obsahovat alespoň jednu číslici</label>
  <label htmlFor="theID" class="sub">Heslo musí obsahovat alespoň sedmncáct trpaslíků</label>
</div>
````
## Options
### Icons
For inserting icons into inputs, place it into span.input-icon. To center it to right, add .right.

### Success x danger
K vyjádření úspěchu nebo chyby můžete k jakémukoli prvku přidat .success nebo .danger
""" TODO: Tady hoď ukázky! """


## Design guidelines
``` css 
.input .icon {
    color: /* SEM DEJ SVUJ STYL */;
}

.input.danger input,
input.danger {
    border-color: var(--danger-color);
}
  
.input.danger label.sub,
label.sub.danger {
    color: var(--danger-color);
}

.input.success input,
input.success {
    border-color: var(--success-color);
}
  
.input.success label.sub,
label.sub.success {
    color: var(--success-color);
}

input.danger,
textarea.danger {
    border-color: var(--danger-color);
}  

input.success,
textarea.success {
    border-color: var(--success-color);
}

input.success:focus,
textarea.success:focus {

}  

input.danger:focus,
textarea.danger:focus {

}

input,
textarea {

}
  
input:focus,
textarea:focus {

}
  
input.editable {

}
  
input.editable:focus {

}

```
