
I'm going to talk about SCSS(Sassy CSS(cascade style sheet)), which is the latest syntax for Sass (syntactically awesome style sheets)

SCSS is the newer syntax of Sass.

what does sass do?
preprocessor scripting language that is compiled into CSS. 

Preprocessing, in this context, is used to help you create css in an efficient, robust and maintainable way.
They have various features that are not availible in CSS.

Sass is one of several CSS preprocessors(such as Less or Stylus)

The features that Sass brings to the table:

## Nesting:

With sass you can nest your CSS selectors, if you've seen regular CSS you know that it can be a mess.

Instead of having to type a selector and then a child selector umpteen times, you can enter the parent selector once, and nest the child selectors inside of it.

    nav {
      ul {
        margin: 0;
        padding: 0;
        list-style: none;
      }

      li { display: inline-block; }

      a {
        display: block;
        padding: 6px 12px;
        text-decoration: none;
      }
    }


## Modules

with sass you can create partials that aren't generated into seperate css files, multiple scss files as modules and import them with `@use`

### mix-ins
  Some things in CSS are a bit tedious to write, especially with CSS3 and the many vendor prefixes that exist. A mixin lets you make groups of CSS declarations that you want to reuse throughout your site.

## Operators
Allow you to do math in css, for example converting pixels into percentaged to create fluid items