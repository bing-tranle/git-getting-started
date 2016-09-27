# Customer Portal Customization Cheatsheet

There is a concrete css file for each customer portal (eg. um.css for University of Maryland, propark.css for Pro Park etc). To make the specific web layout and look and feel for the web content, developer will customize css declaration blocks in css location file to make layout corresponds with coloring style of customer portal.

Almost structured css elements are defined in ~Content/css/base.css so to customize portal layout developer just modifies coloring property and set coloring value.

## Background for Whole Page
It's better if background and font style of body element is overrided for each customer portal, the rest of color style on portal page should be based on body's background color to make best contrast visualization.
~~~css
body {
  color: #4c0006;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 14px;
  background-color: #7b3c3c;
}
~~~

## Page Header
Modify below css declaration blocks to customize background and logo image of customer portal on page header:
~~~css
#Page_Top {
  background-color: #7f0000;
}

#Page_Header {
    background-color: #8A0000;
	background-image: url('images/customer_org_logo.png');
	background-attachment:scroll;
	background-position: 0px 0px;
}
~~~

## Navigation Bar
Below css declaration blocks are used to customize secific style for naviation bar on header:

**Defautl state** of naviation button link style
~~~css
#Page_Header_Menu ul li a.Button {
  background: #b29896;
  color: #ffffff;
}
~~~

**Hover state** of naviation button link
~~~css
#Page_Header_Menu ul li a.Button:hover {
  background: #c8b5b3;
}
~~~

**Active state** of navigation button link
~~~css
#Page_Header_Menu ul li a.Button.active {
  background: #ffffff;
  color: #ff6a4c;
}
~~~

## Page Separator
There is a separator line to split page header and page content, to customize it's style just modify this css bock:
~~~css
#Page_Separator {
  background-color: #ffffff;
}
~~~

## Heading Style
To override section heading, update below css bock in css file of specific location (e.g below is section header definition in um.css):
~~~css
h1 {
  background-color: #8A0000;
}
~~~

## Button Style
Currently, Frequent Parker layout has many css block for button definition, to make all of them consistent override declaration listed below:

Bootstrap button style
~~~css
.btn-primary {
    background: #ff6a4c;
    border-color: #e52600;
    color: #ffffff;
}

.btn-primary:hover {
    background: #ff5532;
    border-color: #e52600;
}

.btn-info {
    background: #9d4c4c;
    color: #ffffff !important;
    border-color: #9d4c4c;
}

.btn-info:hover {
    background: #8c4444;
    border-color: #9d4c4c;
}
~~~

Customer Portal button style
~~~css
a.SmallButton {
    color: #ffffff;
    background: #ff6a4c;
}

input.Button {
    background-color: #ff6a4c;
    color: #ffffff;
}

input.Button:hover {
    background: #ff5532;
}

#submit {
    background: #ff6a4c;
}

#submit:hover {
    background: #ff5532;
}
~~~

## Link Style
If backgound for whole page is same color with default link color, the css style for a link should be modified to make layout display more contrast as possible:
~~~css
a {
    color: #ff6a4c;
}

/*This block also is used to override button style*/
a.primary {
    color: #ff6a4c;
}
~~~

## Account Menu
Override below css declaration blocks to make menu panel on account page layout become consistency with home layout

Modify *color* property to override background color for account menu list
~~~css
.side-block.col-md-3 h4 {
    color: #f9ebee;
}
~~~

Customize account menu heading item
~~~css
    .side-block.col-md-3 h3,
    .side-block.col-md-3 h4 {
    background: #4c0006;
    color: #ffffff;
}
~~~

Customize account menu item style
~~~css
#my_account_nav .list ul li a {
    color: #ffffff;
}
#my_account_nav .list ul li a:hover {
    background: #9d4c4c;
}
#my_account_nav .list ul li a.active {
    background: #ffffff;
    color: #ff6a4c;
}
~~~

## Telerik CSS
Below are some important css blocks which must be overrided to make ui consistency when using telerik component.

Note that this overriden css should be placed in specific telerik css file (e.g telerik.propark.css) other than location css file (e.g propark.css)

~~~css
/* customize color for telerik dropdown control here */
.t-dropdown.t-header {
    background: #8a0000;
}

.t-dropdown.t-header:hover {
    background: #bd6f85;
}

/* customize color for shopping cart here */
.t-widget.t-menu {
    background: #ff6a4c;
}

.t-widget.t-menu li a {
    color: #ffffff;
}

.t-widget.t-menu li a:hover {
    background: #ff6a4c;
}
~~~

## Page Footer
To make page footer display consistency, below css block should be customized
~~~css
footer {
    background-color: #7b3c3c;
    color: #ffffff;
}

footer a {
    color: #ffffff;
}

.footer-wrapper {
    background-color: #7f0000;
}

.footer-secondary {
    background-color: #4c0006;
}
~~~

