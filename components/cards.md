# Cards
There's nothing complicated when working with cards. Just wrap the content into div.card. And if you want more complicated cards, use .card.layout.
``` html sample
<div class="card">
  <h4>Default card</h4>
  <p>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maiores autem tempore dolorum nam voluptate a fuga excepturi esse. Ipsum possimus fuga quam esse, quia quae commodi molestias. Obcaecati, quae tempora?
  </p>
</div>
````
## Structure
``` html
<div class="card">
  <h4>Default card</h4>
  <p>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maiores autem tempore dolorum nam voluptate a fuga excepturi esse. Ipsum possimus fuga quam esse, quia quae commodi molestias. Obcaecati, quae tempora?
  </p>
</div>
````
## Options
### Styles
In default BESAMEL cards levitate on hover. You can also add .primary .secondary or .tertiary .
``` html sample
<div class="card primary">
  <h4>Default card</h4>
  <p>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maiores autem tempore dolorum nam voluptate a fuga excepturi esse. Ipsum possimus fuga quam esse, quia quae commodi molestias. Obcaecati, quae tempora?
  </p>
</div>
<div class="card secondary">
  <h4>Default card</h4>
  <p>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maiores autem tempore dolorum nam voluptate a fuga excepturi esse. Ipsum possimus fuga quam esse, quia quae commodi molestias. Obcaecati, quae tempora?
  </p>
</div>
<div class="card tertiary">
  <h4>Default card</h4>
  <p>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maiores autem tempore dolorum nam voluptate a fuga excepturi esse. Ipsum possimus fuga quam esse, quia quae commodi molestias. Obcaecati, quae tempora?
  </p>
</div>
````
### Layout 
For more complicated cards I created card.layout
``` html sample code
                        <div className="card layout hover primary w-4">
                            <div className="card-head">
                                <img src="https://cataas.com/cat/says/hello%20world!" alt="" />
                            </div>
                            <div className="card-body">
                                <h4>Layout card</h4>
                                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aspernatur laborum possimus dolore doloribus ipsa quo. Lorem ipsum dolor sit amet.</p>
                           </div>
                            <div className="card-footer row space-between">
                                <p>Footer</p> 
                               <h3 className="g-icon hover-show">east</h3>
                            </div>
                        </div>
````

## Design guidelines
``` css
.card {

}
  
.card:hover {

}
  
.card.primary:hover,
.card.secondary:hover,
.card.terciary:hover {

}
  

.card.primary {
  
}
  
.card.secondary {

}
  
.card.terciary {

}
```
