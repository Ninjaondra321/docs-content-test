# Dropdown
You can use dropdown for displaying elements that you want to see after you click on button - like a dropdown menu. Note: this is little different from navbar dropdown.

``` html sample
<div class="dropdown">
	<button class="dropdown-button">Dropdown</button>
	<div class="dropdown-window">
		<a href="#">Link 1</a>
		<a href="#">Link 2</a>
		<hr />
		<a href="#">Link 3</a>
	</div>
</div>
```

## Structure
Using dropdown in your code is not hard. You just put btn.dropdown-button and .dropdown-window inside a .dropdown. Note, that this doesn't handle reactivity yet.
``` html sample
<div class="dropdown">
	<button class="dropdown-button">Dropdown</button>
	<div class="dropdown-window">
		<a href="#">Link 1</a>
		<a href="#">Link 2</a>
		<hr />
		<a href="#">Link 3</a>
	</div>
</div>
```
## Reactivity
You can add onClick event on the dopdown-button, so that every time it's clicked, it runs function (e) => {e.currentTarget.parentElement.classList.toggle("open")}
``` html sample
<div class="dropdown">
	<button class="dropdown-button"
		onClick={(e) => {e.currentTarget.parentElement.classList.toggle("open")}
			>Dropdown</button>
	<div class="dropdown-window">
		<a href="#">Link 1</a>
		<a href="#">Link 2</a>
		<hr />
		<a href="#">Link 3</a>
	</div>
</div>
```