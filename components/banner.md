# Banner
Banners are used to display text, that sould notify the user of some change. Just put div.banner as a first child of nav (find more in [the layout page](/principles/page-layout))
## Structure
``` html
<div class="banner">
  <div class="left"></div>
  <div class="center">
    <header>Nové menu najdete <a href="#">zde</a></header>
  </div>
  <div class="right"><button class="icon small ">close</button></div>
</div>
```

## Design guidelines
Style the banner however you want. It's recommended to use red as a warning, blue for info and colorful for something you the user to see.
``` css
.banner {
	
}

/*Add your classes - such as banner.gradient or whatever */
```
