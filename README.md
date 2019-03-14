# Grid-Based Framework

## Introduction
This is a minimal framework built with SCSS to provide a basic 12-column layout, basic typography styles, and some commonly-used utilities. Our aim was not to recreate [Bootstrap](https://getbootstrap.com/) or to provide an exhaustive collection of styles or resources, but rather to create a lean foundation to build upon.

## Description

### Grid

<ul>
    <li>The grid uses a hierarchy of <code>container</code>, <code>row</code>s, and <code>col</code>umns.</li>
    <li><code>.container</code>s come with 15px padding on each side and a maximum width of 1140px.</li>
    <li>There's a <code>fluid-container</code> option that covers 100% of the width, minus the 15px paddings.</li>
    <li>Rows use flexbox and have 20px gutters between them.</li>
    <li>Column classes are named <code>.col-</code> followed by the number of slots it should span in the grid, from 1 to 12.</li>
    <li>Two breakpoints are included: 480px ('small') and 992px ('medium'). To make columns expand to 100% width in those breakpoints, there are two utility classes: <code>.expand-col-s</code> and <code>.expand-col-m</code>, respectively.</li>
    <li>Columns can be made responsive with ad hoc media queries changing the <code>flex</code> and <code>max-width</code> properties of the desired column. For example:
    <pre>
    <code>
    @media (max-width: 1199.98px) {
        .expand-1199 {
            flex: 0 0 100%;
            max-width: 100%;
        }
    }
    </code>
    </pre>
    This would make the targeted column(s) expand to 100% width for devices with a max-width of 1199.98px.</li>
</ul>

### Typography

<ul>
    <li>Two common types are used, sans-serif for headings and buttons, and serif for most other text.</li>
    <li>Increasing sizes are applied to the headings from <code>h1</code> starting at 24px to <code>h6</code> finishing in 12px.</li>
    <li>Text decorations have been removed from <code>a</code>s, unless on hover.</li>
    <li>Other utilities: <code>.bold</code> and <code>.uppercase</code> are included to increase the font weight to 700 and to transform the text to uppercase, respectively.</li>
</ul>

### Other Utilities

<ul>
    <li>Box-sizing is applied by default.</li>
    <li>There's a <code>.clearfix</code> class that can be applied to containers of floated elements, to clear both floats.</li>
    <li>Different display classes are available for the main display property values, for example: <code>.d-none</code> and <code>.d-flex</code>.</li>
    <li>We've included <a href="https://meyerweb.com/eric/tools/css/reset/">Eric Meyer's reset</a>.</li>
</ul>

## Sample

Using this framework, we've recreated [The Odin Project's homepage](https://www.theodinproject.com/home), as can be viewed [here](https://gferrarocamus.github.io/grid-based-framework/sample-page/index.html).

Created by [Giuliana](https://github.com/gferrarocamus) and [Valentino](https://github.com/1ba1)
