# **islandAQUAdesign**
**islandAQUAdesign** is a website whose purpose is to introduce amateur aquarists to the sub-genre of aquascaping.  
It aims to give the site user: 
- A broad overview of the aquascaping hobby. 
- The core materials used.
- An overview of popular style arrangements.  
- Suitable flora and fauna for a beginner.
- Embedded links that provide launching points to explore other sites to the hobby in more detail.

![Mockup](/assets/images/website_mockup.PNG "Website preview at different resolutions") 

***

## **Existing Features**

- #### **Header logo & Navigation**
    - The *header* logo automatically sizes with the viewport on all resolutions.
    On mobile and tablet the header is *fixed* to keep navigation accessible via the hamburger icon.  
    It also serves as a link to to the top of page as the website is on one page.

    - The site has two Navigation bar styles.  A Hamburger style for mobile and tablet screens with limited screen space and a standard navbar as viewed on the desktop landing page in the next section.

![Mockup](/assets/images/mobile_tablet_nav.PNG "Preview of header/nav with logo at mobile/tablet resolutions")

***

- #### **Landing page**
The *landing page* hero background is designed to draw the user into the topic as a picture paints a thousand words.
As a hobby, a good aquascape is aesthetically pleasing therefore conveys an implicit message to the visitor.

On loading the website, note the subtle use of greyscale fading into the standard contrast to emphasise the beauty of nature.

![Mockup](/assets/images/landing_page.PNG "Website landing page and preview of header/nav at desktop resolution") 

- #### **Footer**
    - The footer offers the user three options:
        - A Means to provide an email address to sign-up to a newsletter.
        - Links that open to new social media tabs for yet to be developed supporting content.
        - A link to the rop of the page by clicking the favicon.

![Mockup](/assets/images/footer_img.PNG "Footer section") 

***

- #### **CSS Grid to layout desktop site**
    - 

![Mockup](/assets/images/grid_view_chrome_dev_tools.PNG "Image of Grid view enabled using Google Chrome developer Tools section")

***

#### Colour Scheme
The colour schema was devised by taking an image of the creators home aquarium.
This image was passed through <https://color.adobe.com/create/image-gradient>

![Mockup](/assets/images/colour_scheme_genetated_from_home_aquarium.PNG "Website landing page")

For font accesibility purposes the above colour scheme was passed to eightspapes.com for the following output:
 <https://contrast-grid.eightshapes.com/?version=1.1.0&background-colors=&foreground-colors=%23FFFFFF%2C%20White%0D%0A%23F2F2F2%0D%0A%23DDDDDD%0D%0A%23CCCCCC%0D%0A%23888888%0D%0A%238C4830%0D%0A%2360731A%0D%0A%23AEBF88%0D%0A%2370A61F%0D%0A%235%0D%0A&es-color-form__tile-size=compact&es-color-form__show-contrast=aaa&es-color-form__show-contrast=aa&es-color-form__show-contrast=aa18&es-color-form__show-contrast=dnp>






## Testing

### Validator Testing
    HTML
        Passed through the offical W3C validator - 11 errors cleared pon 217.8.21 17:30
    CSS
        Passed through the offical Jigswa validator - 66 errors to clear on 27.8.21 18:00
            mostly invalid rgb functions using variable - root:  for example --theme-five: 112, 166, 31;   background-color: rgba(var(--theme-five), 1);

### Unfixed Bugs
    Mobile nav menu
        Menu does not collapse after selecting link then focusing on other part of page. Hamburger icon must be clicked again to uncheck hidden checkbox
        No know fix using CSS only, JS required judging by search of stack overflow.

        W3C CSS Validation service showing errors for all css rgba values.  Variables were used for reusability. (do screenshot)

## Deployment