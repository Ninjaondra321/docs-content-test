## Structure
``` html
<div class="accordion-nice">
  <div key="0" class="accordion-item opened" xd="0">
    <button class="accordion-header ">Title</button>
    <div class="accordion-content">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, sequi quaerat. Possimus hic, quaerat ut eos repellat sint minus doloremque beatae fuga mollitia nulla perferendis commodi quibusdam sequi? Saepe, est!</div>
  </div>
  <div key="1" class="accordion-item closed" xd="0">
    <button class="accordion-header ">Title 02</button>
    <div class="accordion-content">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, sequi quaerat. Possimus hic, quaerat ut eos repellat sint minus doloremque beatae fuga mollitia nulla perferendis commodi quibusdam sequi?
      Saepe, est!
    </div>
  </div>
</div>
```

## Options



## Design guidelines
``` css
.accordion-nice .accordion-item {
    margin: 5px;
    border: solid 1px var(--primary-color-static);
    /* Nevím proč to tak je, ale nech to tu! */
    border-radius: calc(var(--border-radius-components)* 1.2);
}

  .accordion-nice .accordion-header {
    background: var(--primary-color) !important;
    color: var(--font-color-light);
    padding: 10px;
    border-radius: var(--border-radius-components);
    transition: all 0.2s ease-in-out;
}
```

## JSX component
If you're using React, Solid or another js framework, you can take this jsx component as inspiration.

``` jsx
/* THIS IS A SOLIDJS COMPONENT - DOESN'T WORK WITH REACT */

import { createSignal, mergeProps, Match } from "solid-js";

function Accordion(props) {
    const merged = mergeProps({
        oneOpened: false, open0: true,
        contents: [
            { header: "Accordion", content: <p>Ahojj</p> },
            { header: "Accordion", content: <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus perferendis provident ipsa nam, impedit fugit placeat assumenda fugiat! Soluta ex numquam aperiam quae itaque aliquam nulla laborum doloribus culpa deserunt?</p> },
            { header: "Accordion", content: <h4> Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid voluptatem quae aspernatur dolores, tenetur eius eligendi ipsa facilis deleniti suscipit, unde quas. Ad ratione perspiciatis atque adipisci, ullam laborum deleniti!</h4> },
        ]
    }, props);
 
    const [openedID, setOpenedID] = createSignal(merged.open0 == true ? 0 : -1);

    function processOpen(id, e) {
        if (merged.oneOpened && openedID() !== id) {
            setOpenedID(id);
        } else if (merged.oneOpened && openedID() === id) {
            setOpenedID(-1);
        }
        else {
            e.target.parentElement.classList.toggle("closed");
        }
    }
  
    return (<>
        <div className="accordion-nice">
            {merged.contents.map((item, index) => {
                return (<div
                    className={
                        "accordion-item " + (merged.oneOpened ? (openedID() === index ? "opened" : "closed") : "closed")
                    }
 
                    xd={openedID()} key={index}>
                    <button className="accordion-header "
                        onTouch={(e) => processOpen(index, e)}
                        onClick={(e) => processOpen(index, e)}
                    >
                        {item.header}
                    </button>
                    <div className="accordion-content">
                        {item.content}
                    </div>
                </div>);
            })}
       </div> 
    </>);
}
  
export default Accordion;
```