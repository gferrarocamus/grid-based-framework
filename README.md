# Grid-Based Framework

## Introduction
This is a minimal framework built with SCSS to provide a basic 12-column layout, basic typography styles, and some commonly-used utilities. Our aim was not to recreate Bootstrap or to provide an exhaustive resource but rather a lean foundation to build upon. We've included [Eric Meyer's reset](https://meyerweb.com/eric/tools/css/reset/).

## Description

### Grid

<ul>
    <li>The build uses a hierarchy of <code>container</code>, <code>row</code>s, and <code>col</code>umns.</li>
    <li>Rows use flexbox and have 20px gutters between them.</li>
    <li>There's a <code>fluid-container</code> that covers 100% of the width, minus the 15px <code>container</code> padding.</li>
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
    <li>Text decorations have been removed from <code>a</code>, unless on hover.</li>
    <li>Other utilities: <code>.bold</code> and <code>.uppercase</code> are included to increase the font weight to 700 and to transform the text to uppercase, respectively.</li>
</ul>

## Other Utilities

<ul>
    <li>Box-sizing is applied by default.</li>
    <li>There's a <code>.clearfix</code> class that can be applied to containers of floated elements, to clear both floats.</li>
    <li>Different display classes are available for the main display property values, for example: <code>.d-none</code> and <code>.d-flex</code>.</li>
</ul>

## Sample

Using this framework, we've recreated [The Odin Project's homepage](https://www.theodinproject.com/home), as can be viewed [here](https://gferrarocamus.github.io/grid-based-framework/).

Created by [Giuliana](https://github.com/gferrarocamus) and [Valentino](https://github.com/1ba1)