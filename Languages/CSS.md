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

| CSS 1 | No Wrapping             | white-space: nowrap;                                                                                                          |
|-------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| CSS 1 | Inline Block Layout     | display: inline-block;                                                                                                        |
| CSS 2 | Max Width               | max-width: 1024px                                                                                                             |
| CSS 2 | Table - Border Collapse | border-collapse: collapse                                                                                                     |
| CSS 2 | Insert Before/After     |  p.chapter:before { content: 'something '; }  a.href[href^="http://"]:after {content: url(/images/Icon_External_Link.png);}   |
| CSS 3 | nth Child               |                                                                                                                               |
| CSS 3 |                         |                                                                                                                               |
| CSS 3 |                         |                                                                                                                               |
| CSS 3 |                         |                                                                                                                               |
| CSS 3 |                         |                                                                                                                               |
| CSS 3 |                         |                                                                                                                               |
| CSS 3 |                         |                                                                                                                               |
| CSS 3 |                         |                                                                                                                               |
| Draft |                         |                                                                                                                               |
| CSS 3 |                         |                                                                                                                               |
|       |                         |                                                                                                                               |