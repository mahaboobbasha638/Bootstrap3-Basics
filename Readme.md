# Bootstrap Essentials
## Bootstrap Grid
- Container
    - Controls the layout
    - adds 15px padding, no never reaches edges.
    - So full width modules don't put in container
    - Two typs of Containers
        - Fluid container
            - Always adjusts with size of the device

                    <div class="container-fluid"></div>

        - Fixed-Width container
            - Specific width size depending on the size of view port

                    <div class="container"></div>

            - 15px padding on each side
            - adjusts to media query breakpoints 
                - width: auto; < 768px width
                - width: 750px; >= 768px width
                - width: 970px; >= 992px width
                - width: 1170px; >= 1200px width


- Rows
    - Allow you to create Horizontal groups 
    - Place within container
    - Should Always include Columns
    - Get rid of container padding

            <div class="row"></div>

- Columns
    - Allow you to create vertical groups

            <div class="col-SIZE-SPAN"></div>

    - it creates 30px gutters
        - 15px on each side
    - (>12) columns wrap
    - Uses col-SIZE-SPAN
        - SIZE Metrics
            - SIZE represents at which break points it has to devide into the columns
            - Extra Small .col-xs- width: auto; < 768px width
            - Small .col-sm- width: ~62px; >= 768px width
            - medium .col-md- width: ~81px; >= 992px width
            - Large .col-lg- width: ~97px; >= 1200px width
            - you can add as many break points as you want.
        - SPAN Metrics
            - Defines how many columns should display.


## Adding diffente break points
- You can add as many break point as you want like
        
        <div class="col-sm-2 col-md-4 col-lg-6"></div>

## Fixing random alignment issues
- By using clearfix and Resoponse utility class like visible-sm-block, hidden-sm we can Fixed
    random alignment issues when heights are not equal.

        <div class="clearfix visible-sm-block"></div>

## Offsetting columns
- On small screen we can add offset to adjust in the middile by adding column offset
        
        <div class="col-xs-offset-3 col-xs-6 col-md col-md-4 col-lg-6"></div>

- We need to clear by adding offset zero in the next break point without affeting further

        <div class="col-xs-offset-3 col-xs-6 col-sm-offset-0 col-md-4 col-lg-6"></div>

## Nesting columns
- We can add rows inside another row and can play with the columns.

## Customizing column order with push and pull
- You can rearrange the section by using push and pull classes
            
        <div class="col-xs-4 col-sm-push-8"></div>
        <div class="col-xs-4 col-sm-pull-8"></div>


# Bootstrap CSS classes

## Heading and body style
- It will look family  Helvetica, Arial after that sans-serif order
- You can use classes h1, h2 etc.. instead of tags
    
        <div class="h1"></div>

- You can use small tag as well as class to differentiate secondary text

        <small>Secondary text</small>

- Lead class will make text different compared to existing.

        <p class="lead"> The practice environment </p>

## Inline text styles
- "Mark" tag will give background color yellow
- "S", "del" tag for strike through text
- "ins", "u" to show insert text 
- "strong", "b" for bold
- "em", "i" for emphosis tag shows with italic

        <mark>practice</mark>
        <s>load</s>
        <del>exercise</del>
        <ins>accessible</ins>

## Alignment, transformation and abbreviations
### Alignment
- We can use alignment classes like "text-left" for floating text to left
    - text-left -> for float left

            <p class="text-left"></p>

    - text-rigt -> for float right
    - text-center -> for center
    - text-justify -> for justify
    - text-nowrap -> for whitespace nowrap (in single line)

### transformation
- We can use transformation classeds to text transformation
    - text-lowercase -> lowercase letters

            <p class="text-lowercase"></p>

    - text-uppercase -> for capitalize
    - text-capitalize -> for firstletter capitalize
### Abbreviations    
- abbr tag uses for abbrivation, on hover it will show complete abbrivation.

        <abbr title="Captain" class="initialism">Capt.</abbr>
  
## Blockquotes
- "blockquote" tag gives the proper indentation 
- by footer tag we can add author as will in proper alignment
- blockquote-reverse class will float right and add indentation in the right

        <blockquote class="blockquote-reverse">
            <p>Quote text</p>
            <footer>Mahaboob Basha</footer>
        </blockquote>

## List style
- "list-unstyled" class will disable the list format, but only that particular level. if you want in sublevels as will we need to add for each level.

        <ol class="list-unstyled">
            <li>list1</li>
            <li>list2</li>
            <ul>
                <li>list3</li>
                <li>list4</li>
            </ul>
        </ol>

- "list-inline" class will keep the all list items in one like and removes the bullets.

        <ol class="list-inline">
            <li>list1</li>
            <li>list2</li>
        </ol>

- by adding "dl-horizontal" class to defination element at certain break point it will breaks into two columns.

        <dl class="dl-horizontal">
            <dt>Lorem</dt>
            <dd>Ipsum dolor sit amet, consectetur adipisicing elit. Esse quo ducimus dolorum dolore ipsam unde, facere explicabo quae natus alias deserunt quibusdam voluptatem, officiis itaque rerum magni eius odio mollitia!</dd>
        </dl>

## styling code 
- we can use kbd tag to create keyboard button look, using var tag italisize the text( for equations).

        <kbd>control-c</kbd>

- Pre tag will keep the text as it is and keep into a block with proper border (to display java script code etc).

        <pre></pre>

- by adding pre-scrollable class it will prove scrollable box.

        <pre class="pre-scrollable"></pre>

# Other CSS Styles
## buttons
- btn class allows the add the buttons style
- Default btn style calsses 
    - btn, btn-default

            <a class="btn btn-default" href="#" role="button">Link</a>
            <button class="btn btn-default" type="submit">Button</button>
            <input class="btn btn-primary" value="Input" type="submit">

- Button content classes 
    - btn-primary
    - btn-success 
    - btn-info
    - btn-warning
    - btn-danger
- Bbutton size classes
    - btn-xs
    - btn-sm
    - btn-md
    - btn-lg
    - btn-block

            <input class="btn btn-primary btn-xs" value="Input" type="submit">

- Button state class
    - active

            <h3 class="btn btn-default active">Active</h3>

- Button disabled class
    - disabled

            <button class="btn btn-default disabled">Disabled Button</button>

## Tables
- "table" class will give proper style to table.
- Class List
    - table-striped
    - table-border
    - table-hover
    - table-condensed
- By adding the contextual classes you can give colors
    - active
    - success
    - info
    - warning
    - danger

            <div class="table-responsive">
                <table class="table table-striped table-hover table-border table-condensed">
                    <thead>
                        <tr></tr>
                    </thead>
                    <tbody>
                        <tr class="primary"></tr>
                    </tbody>
                </table>
            </div>


- By keeping the table inside container class "table-contanier" will make the table responsive.

## Images
- By adding the "img-responsive" class image gets the resonsive style.
- By adding "center-block" will make the image in the center of the column.
- By adding "img-rounded" it added rounded edges.
- By adding "img-circle" it will give circle images.
- By adding "img-thumbnail" it will give circle images.

            <img class="img-rounded img-responsive center-block" src="images/drwinthrop.jpg" alt="Dr Winthrop Photo">

## Helper classes
- text-muted for light color
- Can add contextual colors
    - text-primary
    - text-success ..etc

            <p class="text-primary"></p>

- Can add background colors using contentual colors
    - bg-primary
    - bg-success ..etc

            <p class="bg-success"></p>

- Layout class (ex on image can add)
    - pull-left
    - pull-right
    - center-block

            <img class="pull-left" src="images/field_sm.jpg" alt="Dr Winthrop Photo">

- Can add show/hidden class to show and hide elements
- Class "Invisible" will hide the image but it will take the corresponding space.

## Responsive Utilities
- We can controls the visibility of certain elements using utility classes at that break point
    - VISIBILITY-SIZE(-DISPLAY)
        - Visibility: visible or hidden
        - Size: xs, sm, md, lg, print
        - Display: block, inline, inline-block, print
    - example
        - visible-xs-block shows up element in xs breakpoint as block element
        - hidden-xs hide the element in xs breakpoint
        - Print element will appear when printing the element
            - visible-print-block

                    <span class="h1 visible-xs-block">Lorem</span>
                    <span class="h1 hidden-xs">Lorem</span>

# Styling Forms
## Basic Forms
- "form-control" class will style the inputbox to width and proper padding
- "form-group" class will create little bit of seperation between element 

            <div class="form-group">
                <label for="inputName">Name</label>
                <input class="form-control" id="inputName" placeholder="Name" type="text">
            </div>

## Radio and Check boxes
- Classes "radio", "checkbox" will give the proper alignemnts
- Classes "radio-inline", "checkbox-inline" will display all the radio and checkbox elements in a line
- disabled propery will disable the selection of the elements

            <div class="form-group"> 
                <label class="radio-inline">
                    <input name="options" disabled="" type="radio">
                    One
                </label>
            </div>

## Inline Forms
- "form-inline" class dispaly form inline style but only in min width of 768px.
## Horizontal Forms
- Good for mobile user 
- On desktop we can align in the center label and textbox next to eachother
- On mobile label and textbox one after the Other
- "form-horzontal" will solve that purpose

## Validation Styles
- We can show the validation state to the user within the inputbox itself with color and icons
    - has-warning

            <div class="form-group has-warning">
                <label for="inputName">Name</label>
                <input class="form-control" type="text"
                    id="inputName" placeholder="Your Name">
            </div>

    - has-error

            <div class="form-group has-error">
                <label for="inputName">Name</label>
                <input class="form-control" type="text"
                    id="inputName" placeholder="Your Name">
            </div>

    - has-success

            <div class="form-group has-success">
                <label for="inputName">Name</label>
                <input class="form-control" type="text"
                    id="inputName" placeholder="Your Name">
            </div>

- By adding the control-lable class will affect the same color style to corresponding label.

            <div class="form-group has-success">
                <label class="control-label" for="inputName">Name</label>
                <input class="form-control" type="text"
                    id="inputName" placeholder="Your Name">
            </div>

- We can show the icons as well along with this validation 
- Bootstrap uses the glyphicons

            <div class="form-group has-success has-feedback">
                <label class="control-label" for="inputName">Name</label>
                <input class="form-control" type="text"
                    id="inputName" placeholder="Your Name">
                <span class="glyphicon glyphicon-ok form-control-feedback"></span>
            </div>

## Input groups
- Allow to combine input field together with other elements
- Like label and input filed combine to disaple each other combinedly
    - Example 
           
            <div class="form-group">
                <label for="inputName">Name</label>
                <input class="form-control" type="text"
                    id="inputName" placeholder="Your Name">
            </div>

    - Combining with addon

            <div class="form-group">
                <div class="input-group">
                    <span class="input-group-addon">$</span>
                    <input class="form-control" type="text"
                    id="inputName" placeholder="Your Name">
                </div>
            </div>

    - Combining with button

            <div class="form-group">
                <div class="input-group">
                    <input class="form-control" type="text"
                    id="inputName" placeholder="Enter search term">
                    <span class="input-group-btn">
                        <button class="btn btn-primary" type="button">Search</button>
                    </span>
                </div>
            </div>

## Fieldset
- Fieldset forms the groups
- Can do group operations like complete fieldset elements can disable by addidng disable attribute.

            <fieldset disable>
                <input type="text">
                <input type="button">
                <input type="password">
            </fieldset>

- No need to add for each input box we can add only to fieldset

## Icons
- we can add icons from glyphicons
    
            <span class="glyphicon glyphicon-phone"></span>
            <button type="button"><span class="glyphicon glyphicon-print"></span> Print</button>

# Navigation Components
## dropdown
- By adding dropdown, dropdown-menu class makes list element into dropdown.
- By adding dropdown-header to list will create header lable in dropdown selection.
- By adding divider class can make the seperation line in the list.
- By adding disabled will disable the selection of the item.

            <div class="dropdown">
                <button type="button" data-toggle="dropdown" id="pettype"
                        aria-haspopup="true" aria-expanded="true"
                        class="btn btn-info dropdown-toggle">Pet Type
                <span class="caret"></span>
                </button>
                
                <ul class="dropdown-menu" aria-labelledby="pettype">
                    <li class="dropdown-header">Common</li>
                    <li><a href="#">Cat</a></li>
                    <li><a href="#">Dog</a></li>
                    <li><a href="#">Fish</a></li>
                    <li class="disabled"><a href="#">Birds</a></li>
                    <li role="separator" class="divider"></li>
                    <li class="dropdown-header">Exotic</li>
                    <li><a href="#">Amphibian</a></li>
                    <li><a href="#">Reptile</a></li>
                    <li><a href="#">Other</a></li>
                </ul>
            </div>

    - Button group makes the display caret and button properly and toggle the list as will.

            <div class="btn-group" >
                <button  class="btn btn-info">Search Pet Info</button>
                <button type="button" data-toggle="dropdown" id="pettype"
                    aria-haspopup="true" aria-expanded="true"
                        class="btn btn-info dropdown-toggle">
                <span class="caret"></span>
                </button>
                
                <ul class="dropdown-menu" aria-labelledby="pettype">
                    <li class="dropdown-header">Common</li>
                    <li><a href="#">Cat</a></li>
                    <li><a href="#">Dog</a></li>
                    <li><a href="#">Fish</a></li>
                    <li class="disabled"><a href="#">Birds</a></li>
                    <li role="separator" class="divider"></li>
                    <li class="dropdown-header">Exotic</li>
                    <li><a href="#">Amphibian</a></li>
                    <li><a href="#">Reptile</a></li>
                    <li><a href="#">Other</a></li>
                </ul>
            </div>

## Button Groups
- btn-group makes the group of unified buttons.

            <div class="btn-group">
                <button type="button" class="btn btn-default"><a href="#">Cat</a></button>
                <button type="button" class="btn btn-default"><a href="#">Dog</a></button>
                <button type="button" class="btn btn-default"><a href="#">Fish</a></button>
                <button type="button" class="btn btn-default"><a href="#">Bird</a></button>
            </div>

- btn-group-vertical makes the group of unified buttons in vertical fashion.

            <div class="btn-group-vertical">
                <button type="button" class="btn btn-default"><a href="#">Cat</a></button>
                <button type="button" class="btn btn-default"><a href="#">Dog</a></button>
                <button type="button" class="btn btn-default"><a href="#">Fish</a></button>
                <button type="button" class="btn btn-default"><a href="#">Bird</a></button>
            </div>

- btn-tool bar makes the group into tool bar.

            <div class="btn-toolbar">
                <div class="btn-group">
                    <button type="button" class="btn btn-default"><a href="#">Cat</a></button>
                    <button type="button" class="btn btn-default"><a href="#">Dog</a></button>
                    <button type="button" class="btn btn-default"><a href="#">Fish</a></button>
                    <button type="button" class="btn btn-default"><a href="#">Bird</a></button>
                </div>
                <div class="btn-group">
                    <button type="button" class="btn btn-default"><a href="#">Amphibian</a></button>
                    <button type="button" class="btn btn-default"><a href="#">Reptile</a></button>
                    <button type="button" class="btn btn-default"><a href="#">Other</a></button>
                </div>
            </div>

- btn-justify will take the whole width of the container. But each button should keep in the different button group.

            <div class="btn-group btn-group-justified">
                <div class="btn-group">
                    <button type="button" class="btn btn-default"><a href="#">Cat</a></button>
                </div>
                <div class="btn-group">
                    <button type="button" class="btn btn-default"><a href="#">Amphibian</a></button>
                </div>
                <div class="btn-group">
                    <button type="button" class="btn btn-default"><a href="#">Cat</a></button>
                </div>
            </div>

## Navigaion Types
- Nav class makes the list into navigation. 
- Nav-tab class makes tab form.
- Active makes that particular element as active.
- nav-pills makes the slightly different look adding background color. 
- nav-stacked makes the stackable format. 

            <ul class="nav nav-pills nav-stacked">
                <li><a href="#">Home</a></li>
                <li class="active"><a href="#">Mission</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Staff</a></li>
                <li><a href="#">Testimonials</a></li>
            </ul>

- nav-justified will justify tabs. 

            <ul class="nav nav-pills nav-justified">
                <li><a href="#">Home</a></li>
                <li class="active"><a href="#">Mission</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Staff</a></li>
                <li><a href="#">Testimonials</a></li>
            </ul>

- navbar-inverse make the different backgorund color and active color.

            <nav class="navbar navbar-inverse">
                    <ul class="nav navbar-nav">
                        <li><a href="#">Home</a></li>
                        <li class="active"><a href="#">Mission</a></li>
                        <li><a href="#">Services</a></li>
                        <li><a href="#">Staff</a></li>
                        <li><a href="#">Testimonials</a></li>
                    </ul>    
                </nav>
            </section>

- navbar-nav makes like navigation. 
- navbar-bottom makes the navigation dispaly at bottom. 

            <nav class="navbar navbar-default">
                <ul class="nav navbar-nav">
                    <li><a href="#">Home</a></li>
                    <li class="active"><a href="#">Mission</a></li>
                    <li><a href="#">Services</a></li>
                    <li><a href="#">Staff</a></li>
                    <li><a href="#">Testimonials</a></li>
                </ul>    
            </nav>

- navbar-fixed-bottom makes the navigation dispaly at bottom of the page.
- navbar-fixed-top dispaly at top of the page.

            <nav class="navbar navbar-default navbar-fixed-bottom">
                <div class="container">
                    <ul class="nav navbar-nav">
                        <li><a href="#">Home</a></li>
                        <li class="active"><a href="#">Mission</a></li>
                        <li><a href="#">Services</a></li>
                        <li><a href="#">Staff</a></li>
                        <li><a href="#">Testimonials</a></li>
                    </ul>  
                </div>
            </nav>

## Adding content to navbar
- Navbar-header adds the header to the navigation

            <nav class="navbar navbar-default">
                <div class="container">
                    <div class="navbar-header">
                        <a href="#" class="navbar-brand">
                            Navigation Header
                        </a>
                    </div>
                    <ul class="nav navbar-nav">
                        <li><a href="#">Home</a></li>
                        <li class="active"><a href="#">Mission</a></li>
                        <li><a href="#">Services</a></li>
                        <li><a href="#">Staff</a></li>
                        <li><a href="#">Testimonials</a></li>
                    </ul>  
                </div>
            </nav>

- We can add button in navigation bar

            <nav class="navbar navbar-default">
                <div class="container">
                    <div class="navbar-header">
                        <a href="#" class="navbar-brand">
                            Navigation Header
                        </a>
                    </div>
                    <ul class="nav navbar-nav">
                        <li><a href="#">Home</a></li>
                        <li class="active"><a href="#">Mission</a></li>
                        <li><a href="#">Services</a></li>
                        <li><a href="#">Staff</a></li>
                        <li><a href="#">Testimonials</a></li>
                    </ul>
                    <button class="btn btn-default navbar-btn">Signin</button>
                </div>
            </nav>

- By navbar-form can add forms in navigation bar

            <nav class="navbar navbar-default">
                <div class="container">
                    <div class="navbar-header">
                        <a href="#" class="navbar-brand">
                            Navigation Header
                        </a>
                    </div>
                    <ul class="nav navbar-nav">
                        <li class="active"><a href="#">Mission</a></li>
                        <li><a href="#">Services</a></li>
                        <li><a href="#">Staff</a></li>
                    </ul>
                    <form class="navbar-form navbar-left">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Search">
                        </div>
                        <button class="btn btn-default">Go</button>    
                    </form>
                </div>
            </nav>

- Sub navigation menu as follows

            <nav class="navbar navbar-default">
                <div class="container">
                    <div class="navbar-header">
                        <a href="#" class="navbar-brand">
                            Navigation Header
                        </a>
                    </div>
                    <ul class="nav navbar-nav">
                        <li class="active"><a href="#">Mission</a></li>
                        <li>
                            <a href="#" class="dropdown-toggle" data-toggle="dropdown">Services
                            <span class="caret"></span></a>
                            <ul class="dropdown-menu">
                                <li><a href="#">Service1</a></li>
                                <li><a href="#">Service2</a></li>
                                <li><a href="#">Service3</a></li>
                            </ul>
                        </li>
                        <li><a href="#">Staff</a></li>
                    </ul>
                    <form class="navbar-form navbar-left">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Search">
                        </div>
                        <button class="btn btn-default">Go</button>    
                    </form>
                    
                </div>
            </nav>

## collapsing navigation
- navigation collapse on break point <768px as follows

            <nav class="navbar navbar-default">
                <div class="container">
                    <div class="navbar-header">
                        <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#collapsemenu">
                            <span class="icon-bar"></span>
                            <span class="icon-bar"></span>
                            <span class="icon-bar"></span>
                        </button>                                
                        <a href="#" class="navbar-brand">
                            Navigation Header
                        </a>
                    </div>
                    <div class="collapse navbar-collapse" id="collapsemenu">
                        <ul class="nav navbar-nav">
                            <li><a href="#">Home</a></li>
                            <li class="active"><a href="#">Mission</a></li>
                            <li><a href="#">Services</a></li>
                            <li><a href="#">Staff</a></li>
                            <li><a href="#">Testimonials</a></li>
                        </ul>  
                    </div>
                </div>
            </nav>

## Bradcrumbs
- By Breadcrumb class can create breadcrumbs 

            <ol class="breadcrumb">
                <li><a href="#">home</a></li>
                <li><a href="#">services</a></li>
                <li><a href="#">grooming</a></li>
            </ol>

- By pager class can create left and right navigation 

            <ul class="pager">
                <li class="previous disabled">
                    <a href="#">
                        <span>&larr;</span>Older</a>
                </li>
                <li class="next">
                    <a href="#">
                        <span>&rarr;</span>Newer</a>
                </li>
            </ul>

- By pagination class can create pagination list. 

            <nav>
                <ol class="pagination pagination-sm">
                    <li><a href="#">&laquo;</a></li>
                    <li><a href="#">1</a></li>
                    <li><a href="#">2</a></li>
                    <li><a href="#">3</a></li>
                    <li><a href="#">&raquo;</a></li>
                </ol>
            </nav>

# Media Components
## Jumbotrons
- Class "jumbotron" makes the element to diplay in gray box and adds padding.

            <div class="jumbotron">
                <h2>Our Mission</h2>
            </div>

## Labels and badges
- Lables and badges usufull css components where you want to pass certain information to user.

           <h3>Exotic Pets
                <label class="label label-primary">new</label>
            </h3>
            <p>We offer specialized care for reptiles, rodents, birds, and other exotic pets.</p>
            <a href="">read articles <span class="badge">4</span></a>

## Thumbnails
- By thumbnail class it will dispaly image in thumbnail along with caption.

            <a href="" class="thumbnail">
                <img class="icon" src="images/drwinthrop.jpg" alt="Icon">
                <div class="caption">
                    cpation caption caption 
                </div>
            </a>

## Media
- Media, media-left, media-body classe will play role to align media and text propelry.

            <div class="media">
                <div class="media-left">
                    <a href="" class="media-object">
                        <img class="icon" src="images/drwinthrop.jpg" alt="Icon">
                    </a>
                </div>
                <div class="media-body">
                    <h3 class="media-heading">Exotic Pets</h3>
                    <p> this is description , this is description , this is description , this is description , this is description.</p>
                </div>
            </div>

## Video with responsive embeds
- Can use repsonsive class like embed-responsive to align video properly.

            <div class="col-xs-6 col-sm-4">
                <div class="embed-responsive embed-responsive-4by3">
                    <video class="embed-responsive-item" src="videos/brushing.mp4"
                        autoplay controls muted></video>    
                </div>
            </div>

- We can use with any video element like youtube embed lik as well.

# Content container
## list groups
- convert into standard list group
    
            <div class="list-groups">
                <li class="list-group-item">Cally Reynolds</li>
                <li class="list-group-item">Sydney Bartlett</li>
                <li class="list-group-item">Hunter Newton</li>
            </div>

## panels
- can do proper panalising data like header, body and footer.

            <div class="panel panel-primary">
                <div class="panel-heading">
                    <h3 class="panel-title">Title</h3>
                </div>
                <div class="panel-body">
                    <p>It's panel-default here</p>
                </div>
                <div class="panel-footer">
                    &raquo; <a href="">get appointment</a>
                </div>
            </div>

## well
- it also give poper indentation and border along the background color

            <div class="well well-lg">
                It's panel-default here, and then we just put our content in there and you're going to need to divide the content into different parts so you can have a div with a class of panel-body, and if you want to, you can paste your content in there
            </div>


# Javascript components
## Carousel
- Carousel will take list of images and show them as presenation like slide show etc.

            <div class="carousel">
                <div class="carousel-inner">
                    <div class="item active">
                        <img src="images/carousel-lifestyle.jpg" alt="Lifestyle Photo">
                    </div>
                    <div class="item">
                        <img src="images/carousel-mission.jpg" alt="Mission">
                    </div>
                    <div class="item">
                        <img src="images/carousel-vaccinations.jpg" alt="Vaccinations">
                    </div>
                </div>
            </div>

- By default whatever the item has active class it will show up like above.
- By adding attribute data-ride="carousel"it will do presentation of all.
- Presentation we can control using classe slide to make slider.
- By adding carousel-cpation can have caption for each image.

            <div class="carousel slide" data-ride="carousel">
                <div class="carousel-inner">
                    <div class="item active">
                        <img src="images/carousel-lifestyle.jpg" alt="Lifestyle Photo">
                        <div class="carousel-caption">
                            <h3>Headline</h3>
                            <p>Dummy text dummy text dummy text.</p>
                        </div>
                    </div>
                    <div class="item">
                        <img src="images/carousel-mission.jpg" alt="Mission">
                    </div>
                    <div class="item">
                        <img src="images/carousel-vaccinations.jpg" alt="Vaccinations">
                    </div>
                </div>
            </div>

- By adding carousel-control elements we can have carousel navigation.

            <div class="carousel slide" id="featured">
                <ol class="carousel-indicators">
                    <li data-target="#featured" data-slide-to="0" class="active"></li>
                    <li data-target="#featured" data-slide-to="1"></li>
                    <li data-target="#featured" data-slide-to="2"></li>
                </ol>
                <div class="carousel-inner">
                    <div class="item active">
                        <img src="images/carousel-lifestyle.jpg" alt="Lifestyle Photo">
                        <div class="carousel-caption">
                            <h3>Headline</h3>
                            <p>Dummy text dummy text dummy text.</p>
                        </div>
                    </div>
                    <div class="item">
                        <img src="images/carousel-mission.jpg" alt="Mission">
                    </div>
                    <div class="item">
                        <img src="images/carousel-vaccinations.jpg" alt="Vaccinations">
                    </div>
                </div>
                <a class="left carousel-control" href="#featured" role="button" data-slide="prev">
                    <span class="glyphicon glyphicon-chevron-left"></span>
                </a>
                <a class="right carousel-control"  href="#featured" role="button" data-slide="next">
                    <span class="glyphicon glyphicon-chevron-right"></span>
                </a>
            </div>

- We can control carousel with jquery script.

            $(".carousel").carousel();
            $(".carousel").carousel({
                interval: 2000, //false for no intrevel
                pause: false, //for hover pass carousel
                wrap: false, //after last it will stop
                keyboard: false //to prevent keyboard control
            });

## tabs
- Controlling tab with javascript.

            <ul class="nav nav-tabs">
                <li role="presentation" class="active" >
                    <a href="#tab1" data-toggle="tab">Tab1</a>
                </li>
                <li role="presentation">
                    <a href="#tab2" data-toggle="tab">Tab2</a>
                </li>
                <li role="presentation">
                    <a href="#tab3" data-toggle="tab">Tab3</a>
                </li>
            </ul>
            <div class="tab-content">
                <div role="tabpanel" class="tab-pane active" id="tab1">
                    tab content 1
                </div>
                <div role="tabpanel" class="tab-pane" id="tab2">
                    tab content 2
                </div>
                <div role="tabpanel" class="tab-pane" id="tab3">
                    tab content 3
                </div>
            </div>

## Collapsible Content 
- By collapse class can handle the collapsible content.

            <a href="#exoticpets" data-toggle="collapse" class="btn btn-primary">Exotic Pets</a>
            <div class="collapse" id="exoticpets">
                <p>Collapse content goes here.</p>
            </div>

            <div data-target="#exoticpets" data-toggle="collapse" class="btn btn-primary">Exotic Pets</div>
            <div class="collapse" id="exoticpets">
                <p>Collapse content goes here.</p>
            </div>

## Accordions
- It will prepare proper collapasable panel with hadeaing and body

            <div class="panel-group" id="accordion" >
                <div class="panel panel-primary">
                    <div class="panel-heading" id="headingone">
                        <h4 class="panel-title">
                            <a href="#exoticpets3" data-toggle="collapse" data-parent="accordion">Exotic Pets</a>
                        </h4>
                    </div>
                    <div class="panel-collapse collapse in" id="exoticpets3">
                        <div class="panel-body">
                            <p>Accordiion panel body text goes here.</p>
                        </div>
                    </div>
                </div>
            </div>

- By adding different panels in panel group and corresponding id will handle toggle among list.

            <div class="panel-group" id="accordion">
                <div class="panel panel-primary">
                    <div class="panel-heading">
                        <h4 class="panel-title">
                            <a href="#exoticpets3" data-toggle="collapse" data-parent="#accordion">Exotic Pets</a>
                        </h4>
                    </div>
                    <div class="panel-collapse collapse in" id="exoticpets3">
                        <div class="panel-body">
                            <p>Accordiion panel body text goes here.</p>
                        </div>
                    </div>
                </div>
                <div class="panel panel-primary">
                    <div class="panel-heading">
                        <h4 class="panel-title">
                            <a href="#exoticpets4" data-toggle="collapse" data-parent="#accordion">Exotic Pets</a>
                        </h4>
                    </div>
                    <div class="panel-collapse collapse" id="exoticpets4">
                        <div class="panel-body">
                            <p>Accordiion panel body text goes here.</p>
                        </div>
                    </div>
                </div>
            </div>

## Tooltips
- Tooltip class makes the proper style tooltips.

        <p>Wisdom Pet
            <a href="" data-toggle="tooltip" data-placement="top" title="Text for tooltip, text for tooltip.">Medicine</a>
                strives to blend the best in traditional and alternative medicine in the diagnosis and treatment of companion animals including dogs, cats, birds, reptiles, rodents, and fish. We apply the wisdom garnered in the centuries old tradition of veterinary medicine, to find the safest treatments and cures.
        </p>

- this won't initiate automatically. we need to add jquery script.

         $('[data-toggle="tooltip"]').tooltip();    
    
## Popover
- Unlike the tooltips these things need to click to show the text. 
- this won't initiate automatically. we need to add jquery script.
- Unlike tooltip attribute for you can have title for popover.

        <button type="button" class="btn btn-info" 
                data-container="body" data-toggle="popover" data-placement="top" data-title="Popover Title"
                data-content="We offere text for popover, and it goes here.">
            Popover
        </button>

        $('[data-toggle="popover"]').popover();   

- By adding data-trigger:focus attribute popover will close on clicking outside.
- But this won't work with button, need to add with ancor tag

        <a class="btn btn-info" role="button" tabindex="0"
                data-container="body" data-toggle="popover" data-placement="top" data-title="Popover Title"  data-trigger="focus"
                data-content="We offere text for popover, and it goes here.">
            Popover
        </a>

## Controlling Menus with scrollfix
- By adding data-offset and data-spy can handle floating the navigation always on top.

            <nav class="navbar navbar-default" data-spy="affix" data-offset="500">
            </nav>

- data-spy will hilightlate the element in the naviation on scrolling to that element.

            <body data-spy="scroll" data-target=".navbar-default" data-offset="50">