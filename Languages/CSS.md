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


| CSS 1                 | No Wrapping           |     white-space: nowr |
|                       |                       | ap;                   |
|                       |                       |                       |
| CSS 1                 | Inline Block Layout   |     display: inline-b |
|                       |                       | lock;                 |
|                       |                       |                       |
| CSS 2                 | Max Width             |     max-width: 1024px |
|                       |                       | ;                     |
|                       |                       |                       |
| CSS 2                 | Table - Border        |     border-collapse:  |
|                       | Collapse              | collapse              |
|                       |                       |                       |
| CSS 2                 | Insert Before/After   |     p.chapter:before  |
|                       |                       | { content: 'something |
|                       |                       | '; }                  |
|                       |                       |                       |
|                       |                       |     a.href[href^="htt |
|                       |                       | p://"]:after {        |
|                       |                       |        content: url(/ |
|                       |                       | images/Icon_External_ |
|                       |                       | Link.png);            |
|                       |                       |     }                 |
|                       |                       |                       |
| CSS 3                 | nth Child             |     tr:nth-child(odd) |
|                       |                       |  { }                  |
|                       |                       |     tr:nth-child(even |
|                       |                       | ) { }                 |
|                       |                       |     tr:nth-child(5) { |
|                       |                       |  }       // just the  |
|                       |                       | 5th                   |
|                       |                       |     tr:nth-child(2n+3 |
|                       |                       | ) { }    // every 2nd |
|                       |                       |  starting at 3        |
|                       |                       |     tr:nth-child(-n+4 |
|                       |                       | ) { }    // first 4   |
|                       |                       |                       |
| CSS 3                 | Media Queries         |     <link rel="styles |
|                       |                       | heet" media="(max-wid |
|                       |                       | th: 800px)" href="exa |
|                       |                       | mple.css" />          |
|                       |                       |                       |
|                       |                       |     @media (min-width |
|                       |                       | : 400px) { }          |
|                       |                       |     @media (max-width |
|                       |                       | : 600px) { }          |
|                       |                       |     @media (max-width |
|                       |                       | : 600px) and (orienta |
|                       |                       | tion: landscape) { }  |
|                       |                       |     @media screen and |
|                       |                       |  (min-aspect-ratio: 1 |
|                       |                       | 6/9) { }              |
|                       |                       |     @media print and  |
|                       |                       | (min-resolution: 300d |
|                       |                       | pi) { }               |
|                       |                       |                       |
| CSS 3                 | View Port             |     <meta name="viewp |
|                       |                       | ort" content="width=3 |
|                       |                       | 20" />                |
|                       |                       |                       |
|                       |                       |     @-viewport { widt |
|                       |                       | h: 640px; }           |
|                       |                       |                       |
|                       |                       |     @-ms-viewport { w |
|                       |                       | idth: device-width }  |
|                       |                       |                       |
|                       |                       |     @media (max-width |
|                       |                       | : 699px) and (min-wid |
|                       |                       | th: 520px) {          |
|                       |                       |       @-viewport {    |
|                       |                       |         width: 640px; |
|                       |                       |       }               |
|                       |                       |     }                 |
|                       |                       |                       |
|                       |                       |     @viewport {       |
|                       |                       |         width: 980px; |
|                       |                       |         min-zoom: 0.2 |
|                       |                       | 5;                    |
|                       |                       |         max-zoom: 5;  |
|                       |                       |         orientation:  |
|                       |                       | landscape;            |
|                       |                       |     }                 |
|                       |                       |                       |
| CSS 3                 | Background Gradient   |     background: -webk |
|                       |                       | it-linear-gradient(#4 |
|                       |                       | 44, #000);            |
|                       |                       |     background: -o-li |
|                       |                       | near-gradient(#444, # |
|                       |                       | 000);                 |
|                       |                       |     background: -moz- |
|                       |                       | linear-gradient(#444, |
|                       |                       |  #000);               |
|                       |                       |     background: linea |
|                       |                       | r-gradient(#444, #000 |
|                       |                       | );                    |
|                       |                       |                       |
| CSS 3                 | Border Radis          |     border-radius: 6p |
|                       |                       | x;                    |
|                       |                       |     border-top-left-r |
|                       |                       | adius: 6px;           |
|                       |                       |     border-top-right- |
|                       |                       | radius: 6px;          |
|                       |                       |     border-bottom-rig |
|                       |                       | ht-radius: 6px;       |
|                       |                       |     border-bottom-lef |
|                       |                       | t-radius: 6px;        |
|                       |                       |                       |
| CSS 3                 | div - Colum Count     |     -webkit-column-co |
|                       |                       | unt: 3;               |
|                       |                       |     -moz-column-count |
|                       |                       | : 3;                  |
|                       |                       |     column-count: 3;  |
|                       |                       |                       |
| CSS 3                 | Animations            |     animation-name: s |
|                       |                       | pin;                  |
|                       |                       |     animation-duratio |
|                       |                       | n: 5s;                |
|                       |                       |     animation-iterati |
|                       |                       | on-count: infinite;   |
|                       |                       |     animation-timing- |
|                       |                       | function: linear;     |
|                       |                       |                       |
| CSS 3                 | Circle Drawing        | Circles are done      |
|                       |                       | using a 50% border    |
|                       |                       | radius                |
|                       |                       |                       |
|                       |                       |     border-radius:50% |
|                       |                       | ;                     |
|                       |                       |                       |
| Draft                 | [Flexbox](http://css- |     display: flex;    |
|                       | tricks.com/snippets/c |     flex-direction: < |
|                       | ss/a-guide-to-flexbox | row | row-reverse | c |
|                       | /)                    | olumn | column-revers |
|                       |                       | e>;                   |
|                       |                       |     flex-wrap: <nowra |
|                       |                       | p | wrap | wrap-rever |
|                       |                       | se>;                  |
|                       |                       |     ...               |
|                       |                       |                       |
| CSS 3                 | Font Smoothing        |     body {            |
|                       |                       |         -webkit-font- |
|                       |                       | smoothing: antialiase |
|                       |                       | d;                    |
|                       |                       |         -moz-osx-font |
|                       |                       | -smoothing: grayscale |
|                       |                       | ;                     |
|                       |                       |     }                 |
|                       |                       |                       |
