# Badges
Badges are really easy to use. You just wrap the text in span.badge and you're done! This works inside all elements (p, h1,h2, ...) and can be used as notification.
``` html sample
<h1>Badges <span className="badge secondary">NEW</span></h1>
<p>Notifications<span className="badge ">NEW</span> </p>
<h2>Primary<span className="badge primary">15+</span></h2>
<h2>Secondary<span className="badge secondary">15+</span></h2>
<h2>Terciary<span className="badge tertiary">15+</span></h2>
```
## Structure
``` html
<h1>Badges <span className="badge secondary">NEW</span></h1>
<p>Notifications<span className="badge ">NEW</span> </p>
<h2>Primary<span className="badge primary">15+</span></h2>
<h2>Secondary<span className="badge secondary">15+</span></h2>
<h2>Terciary<span className="badge tertiary">15+</span></h2>
```
## Options
For better use, it's reccomended to style primary, secondary and tertiary. Default should be primary.

## Design guidelines
``` css
.badge {
	
}

.badge.secondary{

}

.badge.tertiary {

}
```
