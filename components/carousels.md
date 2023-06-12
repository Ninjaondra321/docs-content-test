# Carousel
Carousels are nice. What else do you want me to write here!?
## Structure
Once again, there's nothing hard with building carousels. You just wrap your carousel items in .carousel

The structure is a little bit tricky, because you have to wrap the .carousel into .carousel-parent . This is because of other elements like arrows, that control it's behavior (left and right sliders)
``` html

<div class="carousel ">
  <div class="card w-500px m-w-12">
    <h4>Card header</h4>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum eius enim ostrum, dolorum ex fuga facilis     pariatur animi, tempore maiores esse dolor dolore sapiente quaerat repudiandae incidunt reiciendis eveniet
      explicabo!</p>
  </div>
  <div class="card w-500px m-w-12">
    <h4>Hello World</h4>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum eius enim ostrum, dolorum ex fuga facilis
      pariatur animi, tempore maiores esse dolor dolore sapiente quaerat epudiandae incidunt reiciendis eveniet
      explicabo!</p>
  </div>
  <div class="card secondary w-500px m-w-12">
    <h4>Hello World</h4>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum eius enim ostrum, dolorum ex fuga facilis
      pariatur animi, tempore maiores esse dolor dolore sapiente quaerat epudiandae incidunt reiciendis eveniet
      explicabo!</p>
  </div>
  <div class="card w-500px m-w-12">
    <h4>Hello World</h4>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illum eius enim ostrum, dolorum ex fuga facilis
      pariatur animi, tempore maiores esse dolor dolore sapiente quaerat epudiandae incidunt reiciendis eveniet
      explicabo!</p>
  </div>
</div>
```
## Options
.maximised makes it one children at once
.fade-edge fades edge


## Design guidelines
``` css
.carousel-control-l,
.carousel-control-r {

}

.carousel-parent .left-control:hover .carousel-control-l,
.carousel-parent .right-control:hover .carousel-control-r {

}

.carousel::-webkit-scrollbar {

}

.carousel::-webkit-scrollbar-thumb {

}
  

.carousel::-webkit-scrollbar-thumb:hover {

}

```


## JSX Component
``` jsx
/* THIS IS A SOLID-JS CODE -- DOESN'T WORK WITH REACT OR SOMETHING ELSE*/
  
export function CarouselWrap({ maximised = false, children }) {
    let carouselRef;
    function scrollLeft() {
        carouselRef.scrollLeft = carouselRef.scrollLeft - carouselRef.clientWidth + 50;
    }
    function scrollRight() {
        carouselRef.scrollLeft = carouselRef.scrollLeft + carouselRef.clientWidth - 50;
    }
  
    let pos = { top: 0, left: 0, x: 0, y: 0 };
  
    function mouseDownHandler(e) {
        pos = {
            left: carouselRef.scrollLeft,
            x: e.clientX
        }
  
        document.addEventListener('mousemove', mouseMoveHandler);
        document.addEventListener('mouseup', mouseUpHandler);
    }
  
    const mouseMoveHandler = function (e) {
        // How far the mouse has been moved
        const dx = e.clientX - pos.x;
        carouselRef.scrollLeft = pos.left - dx;
    };
  
    const mouseUpHandler = function () {
        document.removeEventListener('mousemove', mouseMoveHandler);
        document.removeEventListener('mouseup', mouseUpHandler);
  
        carouselRef.style.removeProperty('user-select');
    };
  
 
 
    return (<div style="position:relative; height:100% " class="carousel-parent">
        <style>
            {`
            .carousel-parent * {
                user-select: none;
            }
            `}
        </style>
        <div className="left-control m-hidden" onClick={scrollLeft}>
            <button class="carousel-control-l"  >chevron_left</button>
        </div>
        <div className="right-control m-hidden" onClick={scrollRight}>
            <button class="carousel-control-r"  >chevron_right</button>
        </div>
        <div className={"carousel " + (maximised ? " maximised" : "")} ref={carouselRef} onmousedown={mouseDownHandler}>
            {/* {props.children} */}
            {children}
        </div>
    </div>);
}
```
