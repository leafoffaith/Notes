---
description: JS and CSS Snippets to remember
---

# React Learning Notes & More

To make something hover on top of another thing like below

The \<div> underneath should be relative and the \<div> SOLD OUT should be absolute inside the outer \<div>

```jsx
export default function Card(props) {
    return (
        <div className="card">
            <div className="card--badge">SOLD OUT</div>
            <img src={`../images/${props.img}`} className="card--image" />
            <div className="card--stats">
                <img src="../images/star.png" className="card--star" />
                <span>{props.rating}</span>
                <span className="gray">({props.reviewCount}) • </span>
                <span className="gray">{props.location}</span>
            </div>
            <p className="card--title">{props.title}</p>
            <p className="card--price"><span className="bold">From ${props.price}</span> / person</p>
        </div>
    )
}
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bfe72c23-5a2c-4591-b69b-b90ad42fc754/Untitled.png)



LOGICAL &&

{props.openSpots === 0 && \<div className="card--badge">SOLD OUT\</div>}

In the code snippet you provided, **`&&`** is a logical AND operator. It is used to conditionally render the **`<div className="card--badge">SOLD OUT</div>`** element based on the result of the expression **`props.openSpots === 0`**.

Here's how it works: if **`props.openSpots`** is equal to 0 (i.e., there are no open spots available), then the first part of the expression **`props.openSpots === 0`** will be true. The logical AND operator **`&&`** then evaluates the second part of the expression (**`<div className="card--badge">SOLD OUT</div>`**) since both parts of the expression are true. This causes the **`<div>`** element to be rendered.

On the other hand, if **`props.openSpots`** is not equal to 0 (i.e., there are open spots available), then the first part of the expression **`props.openSpots === 0`** will be false. Since the logical AND operator **`&&`** requires both parts of the expression to be true in order to evaluate the second part of the expression, the **`<div>`** element will not be rendered.

So, essentially, the **`&&`** operator in this case is being used to conditionally render the "SOLD OUT" badge based on whether or not there are any open spots available.



Spread Syntax with object literals while passing props

```jsx
export default function App() {
    const cards = data.map(item => {
        return (
            <Card
                key={item.id}
                {...item}
                
            />
        )
    })
```
