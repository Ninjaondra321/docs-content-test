
Vstupy v BEŠAMELu mají pevně daný pořádek. V div.input vložte po pořadí label, input popř. label.sub

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
#### Icons
Jestli chcete přidat ikonu do inputu, tak nad input vložte span.icon nebo span.icon.right

#### Success x danger
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

## Part from BEŠAMEL
```

```
