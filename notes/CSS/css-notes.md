# **_Padding and margin_**

- **Padding** is the space between elements content and border
- **Margin** is the space between border and surrounding elements
- **Negative Margin**
  > `margin: -10`  
  > allows the element to grow and push into surrounding elements, rather than conform relative to the boudaries of the element.  
  > It can be used to make a header which spans the full width of an entire container for example.
- **Clockwise notation for padding and margin**

  > `padding: 10px 20px 10px 20px`  
  > sides are arranged in clockwise order starting at the top:  
  > `padding: 10px(top side) 20px(right side) 10px(bottom) 20px(left side)`

- **Reference:**

  > Apply to all four sides  
  > padding: 1em;

  > vertical | horizontal  
  > padding: 5% 10%;

  > top | horizontal | bottom  
  > padding: 1em 2em 2em;

  > top | right | bottom | left  
  > padding: 5px 1em 0 2em;

# **_CSS Units_**

In CSS there are **_relative units_** and **_absolute units_**.

- **_Relative units_** are generally the best to use in modern CSS, particularly when working with responsive web design. Their size is relative to other units, so can resize easily with different portal sizes. They are relative to their **_parent element_**.
- **_Absolute units_** Stay the same size.
- [Link to docs for all units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#what_is_a_css_value)

### **Relative units:**

- **_Percentages:_**
  `width: 50%` = half the width of the parent  
  `line-height: 50%` = half of the font-size of the element.

- **_em:_**  
  `font-size: 1em` = font-size of parent  
  `font-szie: 2em` = 2 x parent font-size  
  `font-size: 3em` = 3 x parent font-size

  - can be used with other elements but using the computed font-size of the parent element.
  - when used with nested element, it multiplies with each child, leading to runaway font sizes.

- **_rem (root ems):_**

  - Relative to the root html element, so avoids nested elemet problem of `em`
  - If root font-size is 20px:
    - 1rem = 20px (always)
    - 2rem = 40px (always)
  - `rem` allows all sizes (ideal for font-size but not limited to it) to scale responsively; if user increases font-size with zoom, in their browser, it will all scale.
  - Not ideal for individual customisation of elements, where `em` becomes relevant.

- **_vw (view width) & vh(view height)_**
  - `1vw` = 1% of viewport width
  - `1vh` = 1% of viewport height
  - can be used in nesting, but `percentage` may be easier for divying up the space.

# **Overide styles**

- a class can over-ride a body
- there is a heirarchy of classes; top one take top priority:

  > .test {color: green;}  
  > p {color: red;}

  - text would be green.

  > .test {color: green;}  
  > p {color: red !important;}

  - text would be red.

# **Custom CSS Variables**

- Define a value in a single place and reference it throught the document.
- Don't need to rely on preprocessors as much (SASS).
- provides cleared semantic meaning.
- Syntax:

  > to _define_:  
  >  body {

      --main-page-color: purple;

  }

  > to _use_:  
  >  h1 {  
  >  background-color: var(--main-page-color);  
  >  }

- To create a fallback if inital isn't compatible (and to help debug):

  > `background: var(--penguin-skin, black);`

- It is best practice to allow for **_browser compatibility_** issues. Back up the variable with a normal css declaration:

  > background: red;  
  >  background: var(--red-color);

- To use _Globally_:
  > :root {  
  >  --main-page-color: purple;  
  > }
- to use _Locally_(particular element of section):
  - can be used in child
  - locally declared variable will override global scope.
  - `--main-page-color: black;` inside element.

# Responsive Web Design

## Media Queries

[link to docs](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)

`@media <media type>(<condition>){<css rules>}`  
`@media screen and (max-width:500px){}`  
`@media (max-width: 100px) { /_ CSS Rules _/ }`  
`@media (min-height: 350px) { /_ CSS Rules _/ }`

    @media (max-height: 800px) {
      p {
        font-size: 10px;
      }
    }

- Responsive image:

        img {
          max-width: 100%;
          height: auto;
        }

- Images for High-Resolution displays (e.g. Retina display):

  - Half width and height of original image.

- Use relative units

### Media Queries - Hierarchy

1.  top media queries are prioritized by order, for example:

        @media screen and (max-width:800px){
          h1 {
            color: cyan;
          }
        }

        @media screen and (max-width:500px){
          h1 {
            color: green;
            font-size: 5rem;
          }
        }

2.  Alternatively they can be combined into a single entry(counteracts hierarchy):

        @media screen and (min-width:500px) and (max-width:800px){
          h1 {
            color: orangered;
          }
        }
