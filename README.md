# **islandAQUAdesign**

Welcome to **islandAQUAdesign**. A website developed to introduce amateur aquarists to the popular sub-genre of aquascaping.

![Mockup](docs/readme/website_mockup.png "Website preview at different resolutions") 


# UX Design

As a topic aquascaping is too expansive to contain within one small site given project time constraints and the developers recognition of their current skill level.

A conscious decision was taken to generalise content and not be too technical as this could dissuade the aspiring hobbyist.

Using UX principles, *user stories* narrowed the *scope* of the site directing it to provide:
- A broad overview of the aquascaping hobby.
- The core materials used.
- An overview of popular style arrangements.  
- Suitable flora and fauna for a beginner.
- Embedded links that provide launching points to explore other sites to the hobby in more detail.

## Wireframing
- To follow best practice, wireframes were developed for mobile / tablet and desktop based on the webinar of the project lead Matt Boden at the [Code Institute](https://www.codeinstitute.net/). Using his advice the mobile site was developed before the desktop.
- Wireframes were created using [Balsamiq Cloud](https://balsamiq.cloud/sqiyfsu/pr12ogh/r2278#). I went a little further almost to mockup level to help visualise the development needed.  Having the *skeleton* in place focused subsequent coding. (Note I consider it fair to admit I abandoned a previous iteration of the project as it lacked direction and was proving to be frustrating. This was a good early learning experience which deserves mentioning). UX defines proper development practices!

## Color Scheme and Accessibility
- The *color scheme* was devised by taking an image of a home aquarium.
The image was passed to [Adobe Color](https://color.adobe.com/create/image-gradient).
- To meet WCAG 2.0 criteria, the generated colour scheme was then passed to [eightshapes.com](http://www.eightshapes.com) for an [accesibility table](docs/readme/color_scheme.png "Color Accessibilty").

## Code Reusability
- CSS variables were used to improve code reusability.  RGB values were saved into the `:root` level of the external CSS file.  These values were then available when declaring rgbA values.  This is a superior solution as it saves time by changing the code in one place to changes multiple elements simultaneously.  It also provided the option to easily control the *alpha* value if required.
- Classes were reused insofar as possible to promote homogeneity across the site. See below for an example of code utilising css variables.

    ```css
    :root {
        --theme-one: 96, 115, 26;
    }

    h2 {
        background-color: rgba(var(--theme-one),1);
    }
    ```

## CSS Grid used to layout desktop site
At an early stage upon the advice of my mentor, I learned *CSS Grid* in order to develop the [desktop site](docs/readme/desktop_grid_view.png "Image of Grid view enabled using Google Chrome developer Tools section").  Research credited in the content section demonstrates it has  superior responsiveness and is more adaptable for placing future sections than utitising relative/absolute displays and archaic floats.  Consider it a bespoke version of Bootstrap.
I opted to explicity place sections as opposed to declaring grid areas in this instance as the site is small.
Also noted is the importance of *html structure*. Sections that are nested have an affect on the grid behaviour.
Generally *grid* offers more flexibility for moving / adding sections to the site in future and ultimately requires less code. It is more readable therefore is easier to maintain.

# Existing Features

## One Page Site / Future Implementations
Developing a single page site with multiple sections was merely a personal preference. It's considered a *top level* to convey general information.  Future developments could include more technical aspects of being an aquarist maintained on separate pages.  For example, the nitrogen cycle, Co2 injection systems, lighting setups, filtration etc.
Another idea was to fix the header to the top of the desktop page. When hovering/focusing on a particular section the relevant link in the menu would appear active. This would provide the user a further indicatiojn of were they were in the web document.

## Header logo & Navigation
On mobile and tablet the header is *fixed* to keep navigation accessible via the hamburger icon.  
This serves as a link to the home of the website in line with practices intuitive user experience on smaller resolutions.

- The site has two Navigation bar styles.  A Hamburger style for [smaller screens](docs/readme/mobile_tablet_nav.png "Preview of header/nav with logo at lower resolutions") with limited width and a standard navbar as viewed on [desktop](docs/readme/desktop_nav.png "Preview of header/nav for higher resolution screens") sized screens.

## Landing page
- The [*landing page*](docs/readme/landing_page.png "Website landing page and preview of header/nav at desktop resolution") has a hero background to pique the users interest.
A well designed/maintained aquascape is aesthetically pleasing therefore conveys an *implicit* message to the visitor.
- On loading the desktop site, note the subtle use of greyscale fading into the standard contrast to emphasise the beauty of nature.

## External Links
- [*External links*](docs/readme/external_links.png "Links are provided to external sites by clicking the image or its caption") provide a launching point for the user to explore the hobby in more detail. These are popular sources and reputable retailers from the UK.
- Each link opens in a new tab so the user can easily refer back to main site.

## Footer
- The [*footer*](docs/readme/footer.png "Footer section") offers the user three options:
- A means to provide an email address to sign-up to a newsletter. Note an extensive form page isn't needed for the website's purposes.
- Links that open to new social media tabs for yet to be developed supporting content. Social media icons scale up on mouse hover to improve user experience.
- In the desktop site, a link to the top of the page is available by clicking the favicon.  To save space the favicon is hidden in the mobile site.  Additionally it is not required as the fixed header is always available for links.

# Testing

LIGHTHOUSE DONT FORGET TO RUN FINAL CODE THROUGH AND SNAPSHOT!

## Validator Testing
- HTML code passed through the offical [W3C Markup Validator](https://validator.w3.org/). 1 error remaining.  Intentionally left as section meant for holding background image content only.

    ```html
    <section id="hero-bg" class="hero-bg">
        <!-- no heading required as suggested by validator check.  Section to hold a background image only -->
    </section>
    ```
- CSS code passed through the offical [W3C Jigsaw Validator](https://jigsaw.w3.org/css-validator/) - No errors found.

## Fixed Bugs
- Mobile *fixed header* obscured section links leading to a negative user experience.
Utilised a [css only solution](https://codepen.io/cferdinandi/pen/GRJvozN) `scroll-margin-top` to scroll 121px above the section links. Incidentially this is the height of the mobile fixed header + 10px of white background space.

    ```css
    section[id] {
    scroll-margin-top: 121px;    
    }
    ```    
- Email field validation can be bypassed by directly clicking the submit button or pressing enter. To fix this I added `required` to the end of input tag as below.

    ```html
    <input id="email-field" type="email" name="user-email" placeholder="Email address"
                aria-label="Type your email address here" required>
    ```

- At higher resolutions the `.video` class dimensions became [distorted](docs/readme/distorted_video.png) from standard 16:9 aspect ratio in plants section due to being within an `iframe`. For formatting purposes I wanted the video to fill 90% of the screen width at all times.
The dimension issue by solved placing the iframe inside a `div`. The iframe was styled to fit the full height and width of the div which in turn had a `padding-top` value of 56.25%.  This was calcuated using the aspect ratio (9/16 = 0.5625).
Conversly, hard coding a value of 800px for the desktop render the iframe too large on a mobile screen. 

## Unfixed Bugs
- [Mobile nav menu](docs/readme/mobile_nav.png) does not collapse after selecting link then focusing on other parts of page. The menu icon must be clicked again to uncheck the hidden checkbox.
A review of [Stack Overflow](https://stackoverflow.com/) suggests no known fix using CSS only solution and that JavaScript is required.

# Deployment

The site was deployed to *GitHub* pages. The steps to deploy are as follows:
- In the GitHub repository, navigate to the *Settings* tab
- From the source section drop-down menu, select the Master Branch
- Once the master branch has been selected, the page will be automatically refreshed with a detailed ribbon display to indicate the successful deployment.

The live link can be found here - https://stevenweir038.github.io/islandAQUAdesign/index.html

## Local Deployment

In order to make a local copy of this repository, you can clone the project by typing the follow into your IDE terminal:
- `git clone https://github.com/StevenWeir038/islandAQUAdesign.git`

Alternatively if using gitpod you can click [here](https://gitpod.io/#https://github.com/StevenWeir038/islandAQUAdesign)

# Credits

## Content
Learning on the following topics supported by:
- CSS Grid / Responsive Web Design - [Wes Bos](https://www.youtube.com/watch?v=DCZdCKjnBCs) and [Kevin Powell](https://www.youtube.com/watch?v=duH4DLq5yoo)
- CSS variables - [Web Dev Simplified channel on YouTube](https://www.youtube.com/watch?v=oZPR_78wCnY).
- CSS animations - [css-tricks.com](https://css-tricks.com/almanac/properties/a/animation/).
- Responsive Iframes - [w3schools.com](https://w3schools.com/howto/howto_css_responsive_iframes.asp)

Also a special mention for my mentor [Tim Nelson](https://github.com/TravelTimN) for his professionalism and guidance on writing markdown, project deployment, html semantics and improved user experience including [scrolling behaviours](https://css-tricks.com/snippets/jquery/smooth-scrolling/) on one page sites.

## Media


