# islandAQUAdesign 
is a website designed to introduce amateur aquarists with some experience to the sub-genre of aquascaping.  
It aims to: 
    Give a broad overview of the hobby from the materials used
    Popular style arrangements.  
    What plants and animals are suited to a beginner.
    Links that provide launching points to explore other sites therefore the hobby in more detail.

Features

    Header logo

    Navigation Bars Mobile
    Navigation Bars Desktop
    Landing page

    Colour Scheme
        genetated by image of a home aquarium


Used css grid to layout desktop site

Testing

Validator Testing
    HTML
        Passed through the offical W3C validator - 11 errors cleared pon 217.8.21 17:30
    CSS
        Passed through the offical Jigswa validator - 66 errors to clear on 27.8.21 18:00
            mostly invalid rgb functions using variable - root:  for example --theme-five: 112, 166, 31;   background-color: rgba(var(--theme-five), 1);

Unfixed Bugs
    Mobile nav menu
        Menu does not collapse after selecting link then focusing on other part of page. Hamburger icon must be clicked again to uncheck hidden checkbox
        No know fix using CSS only, JS required judging by search of stack overflow.

        W3C CSS Validation service showing errors for all css rgba values.  Variables were used for reusability. (do screenshot)


    Deployment