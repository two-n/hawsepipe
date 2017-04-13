# Hawsehole ⚓

React component for navigation and transitions among named anchors.

`npm install --save hawsehole` (or `yarn add hawsehole`)

All props are optional and documented [in source](src/index.js#L12-L29).

## Example

```jsx
import React from 'react';
import { render } from 'react-dom';
import Hawsehole from 'hawsehole';

render(
  <Hawsehole>
    <a name="constitution"><h1>The Constitution of the United States</h1></a>

    <a name="preamble"><h2>Preamble</h2></a>
    <p>We the People of the United States, in Order to form a more perfect Union, establish Justice, insure domestic Tranquility, provide for the common defence, promote the general Welfare, and secure the Blessings of Liberty to ourselves and our Posterity, do ordain and establish this Constitution for the United States of America.</p>

    <article>
      <a name="article-I"><h2>Article I</h2></a>
      
      <section>
        <a name="article-I-section-1"><h3>Section 1</h3></a>
        <p>All legislative Powers herein granted shall be vested in a Congress of the United States, which shall consist of a Senate and House of Representatives.</p>
      </section>
      
      <section>
        <a name="article-I-section-2"><h3>Section 2</h3></a>
        <p>1: The House of Representatives shall be composed of Members chosen every second Year ...</p>
      </section>

    </article>

  </Hawsehole>
, document.getElementById('container'));
```

Planned features:
- scrolling to anchor on demand via prop
- optionally replacing hash with scrolled anchor, as well as clicked nav option
