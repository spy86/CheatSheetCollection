### Ressources

-   [CSS Layouts](http://learnlayout.com/) Introduction
-   Web - Javascript Online IDE: [JSFiddle](http://jsfiddle.net/)
-   External Link Indicators

        // Set for all links
        .content a[href^="//"]:after, 
        .content a[href^="http://"]:after, 
        .content a[href^="https://"]:after {
            content: url(/images/Icon_External_Link.png);
            margin: 0 0 0 5px;
        }

        // Exclude local links
        .content a[href^="//lzone.de/"]:after, 
        .content a[href^="http://lzone.de/"]:after, 
        .content a[href^="https://lzone.de/"]:after {
            content: '';
            margin: 0;
        }

-   Image Inlining

        <img src="data:image/png;base64,[IMAGE_DATA_STRING]" />

-   CSS Pre-Processors
    -   [Less](http://lesscss.org/)
    -   [Sass](http://sass-lang.com/)
    -   [Stylus](https://learnboost.github.io/stylus/)

### Advanced CSS Style Overview

| Name  | Comment                                                           | Example                                                                                                                                                                                                                                                                                           |
|-------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CSS 1 | No Wrapping                                                       | white-space: nowrap;                                                                                                                                                                                                                                                                              |
| CSS 1 | Inline Block Layout                                               | display: inline-block;                                                                                                                                                                                                                                                                            |
| CSS 2 | Max Width                                                         | max-width: 1024px                                                                                                                                                                                                                                                                                 |
| CSS 2 | Table - Border Collapse                                           | border-collapse: collapse                                                                                                                                                                                                                                                                         |
| CSS 2 | Insert Before/After                                               |  p.chapter:before { content: 'something '; }  a.href[href^="http://"]:after {content: url(/images/Icon_External_Link.png);}                                                                                                                                                                       |
| CSS 3 | nth Child                                                         | tr:nth-child(odd)  { }  tr:nth-child(even |) { } tr:nth-child(5) { }       // just the 5th tr:nth-child(2n+3) { }    // every 2nd starting at 3 tr:nth-child(-n+4) { }    // first 4                                                                                                              |
| CSS 3 | Media Queries                                                     |  <link rel="styles heet" media="(max-width: 800px)" href="example.css" />   @media (min-width: 400px) { } @media (max-width: 600px) { } @media (max-width: 600px) and (orientation: landscape) { } @media screen and (min-aspect-ratio: 1 6/9) { } @media print and (min-resolution: 300d pi) { } |
| CSS 3 | View Port                                                         | <meta name="viewport" content="width=3 20" /> @-viewport { width: 640px; }  @-ms-viewport { width: device-width }    @media (max-width: 699px) and (min-width: 520px) { @-viewport { width: 640px;} } @viewport {width: 980px; min-zoom: 0.25;max-zoom: 5; orientation: landscape;   }            |
| CSS 3 | Background Gradient                                               | background: -webkit-linear-gradient(#4 44, #000);    background: -o-linear-gradient(#444, # 000);    background: -moz-linear-gradient(#444, #000);    background: linear-gradient(#444, #000 );                                                                                                   |
| CSS 3 | Border Radis                                                      | border-radius: 6px; border-top-left-radius: 6px; border-top-right-radius: 6px; border-bottom-right-radius: 6px; border-bottom-left-radius: 6px;                                                                                                                                                   |
| CSS 3 | div - Colum Count                                                 | -webkit-column-count: 3; -moz-column-count: 3; column-count: 3;                                                                                                                                                                                                                                   |
| CSS 3 | Animations                                                        | animation-name: spin; animation-duration: 5s; animation-iteration-count: infinite; animation-timing-function: linear;                                                                                                                                                                             |
| CSS 3 | Circle Drawing                                                    | Circles are done using a 50% border radius border-radius:50%;                                                                                                                                                                                                                                     |
| Draft | [Flexbox](http://css-tricks.com/snippets/css/a-guide-to-flexbox/) | display: flex; flex-direction: <row  row-reverse  column  column-reverse>; flex-wrap: <nowrap wrap wrap-rever se>;                        ...                                                                                                                                                     |
| CSS 3 | Font Smoothing                                                    | body {-webkit-font-smoothing: antialiased; -moz-osx-font-smoothing: grayscale;}                                                                                                                                                                                                                   |
|       |                                                                   |                                                                                                                                                                                                                                                                                                   |