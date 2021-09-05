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
    - The *landing page* hero background is designed to draw the user into the topic as a picture paints a thousand words.
    As a hobby, a good aquascape is aesthetically pleasing therefore conveys an implicit message to the visitor.
    - On loading the website, note the subtle use of greyscale fading into the standard contrast to emphasise the beauty of nature.

![Mockup](/assets/images/landing_page.PNG "Website landing page and preview of header/nav at desktop resolution") 

***

- #### **External Links**
    - *External links* provide a launching point for the user to explore the hobby in more detail. These are carefully selected and reputable.
    - Each link opens in a new tab so the user can easily refer back to main site.

![Mockup](/assets/images/external_links.PNG "Links are provided to external sites by clicking the image or its caption") 

***

- #### **Footer**
    - The *footer* offers the user three options:
        - A Means to provide an email address to sign-up to a newsletter.
        - Links that open to new social media tabs for yet to be developed supporting content.
        - A link to the rop of the page by clicking the favicon.

![Mockup](/assets/images/footer_img.PNG "Footer section") 

***

- #### **CSS Grid used to layout desktop site**
    - *Grid* was utilised to as it has superior responsiveness and is more adaptable for placing sections than using archaic floats etc.
      It offers more flexibility for moving / adding sections to the site in future and ultimately requires less code.

![Mockup](/assets/images/grid_view_chrome_dev_tools.PNG "Image of Grid view enabled using Google Chrome developer Tools section")

***

- #### **Colour Scheme and Accessibility**
    - The *colour scheme* was devised by taking an image of the creators home aquarium.
    The image was passed through <https://color.adobe.com/create/image-gradient>
    - The above colour scheme was then passed to <http://www.eightshapes.com> for the output linked below:
    This was to be sure the site meet WCAG 2.0 criteria.

 <https://contrast-grid.eightshapes.com/?version=1.1.0&background-colors=&foreground-colors=%23FFFFFF%2C%20White%0D%0A%23F2F2F2%0D%0A%23DDDDDD%0D%0A%23CCCCCC%0D%0A%23888888%0D%0A%238C4830%0D%0A%2360731A%0D%0A%23AEBF88%0D%0A%2370A61F%0D%0A%235%0D%0A&es-color-form__tile-size=compact&es-color-form__show-contrast=aaa&es-color-form__show-contrast=aa&es-color-form__show-contrast=aa18&es-color-form__show-contrast=dnp>

![Mockup](/assets/images/colour_scheme_genetated_from_home_aquarium.PNG "Website landing page")

***

## **Testing**
- ### **Validator Testing**
    - HTML
    Code passed through the offical [W3C Markup Validator](https://validator.w3.org/) on 3.9.21 @ 20:15. 2 errors remaining.  Intentionally left as sections meant for holding background image content only.

            <section id="hero-bg" class="hero-bg">
                <!-- no heading required as suggested by validator check.  Section to hold a background image only -->
            </section>
            <section class="left-fish-background">
                <!-- no heading required as suggested by validator check.  Section to hold a background image only -->
            </section>

    - CSS
        - Code passed through the offical [W3C Jigsaw Validator](https://jigsaw.w3.org/css-validator/) - No errors found.

- ### **Fixed Bugs**
    - Mobile/Tablet *fixed header* obscures section links
    - Utilised [css only solution](https://codepen.io/cferdinandi/pen/GRJvozN) **scroll-margin-top** to mitigate.

                section[id] {
                scroll-margin-top: 150px;    
                }

- ### **Unfixed Bugs**
    - Email field validation can be bypassed by directly clicking the submit button in footer. JS needed to prevent activation of submit button prior to email input being correctly populated.
    - *Mobile nav menu* does not collapse after selecting link then focusing on other parts of page. The menu icon must be clicked again to uncheck hidden checkbox
        A review of [Stack Overflow](https://stackoverflow.com/) suggests no known fix using CSS only and that JS is required.
        
        ![Mobile/Tablet nav menu will not collapse when no longer in focus](/assets/images/mobile_nav.PNG)

***

## **Deployment**
- The site was deployed to *GitHub* pages. The steps to deploy are as follows:
    - In the GitHub repository, navigate to the *Settings* tab
    - From the source section drop-down menu, select the Master Branch
    - Once the master branch has been selected, the page will be automatically refreshed with a detailed ribbon display to indicate the successful deployment.

The live link can be found here - https://stevenweir038.github.io/islandAQUAdesign/index.html

***

## **Credits**
- Thankyou you to [Wes Bos](https://www.youtube.com/watch?v=DCZdCKjnBCs) and [Kevin Powell](https://www.youtube.com/watch?v=duH4DLq5yoo) for CSS grid tutorials to develop th desktop site.

### **Content**

### **Media**

***
