#Introduction

The following guide can assist you with structuring and styling content on a page using the AODA Drupal Theme. Many of the recommended code snippets are from the Bootstrap Framework. Visit [Bootstrap CSS](http://getbootstrap.com/css/) for a full list of CSS classes.

# Table of Contents

1. [Buttons](#buttons)
2. [Images](#images)
3. [Slideshows](#slideshows)
4. [Templates](#templates)

# Buttons
![Image of all bootstrap buttons](/images/buttons.jpg)

The following code snippets demonstrate the style classes you would use to style a button or a link so that it looks like a button. You can control the colour and size of each button.

### When to use a button vs a link
If clicking the button causes the user to go to a different page, use a link. 
```HTML
<a href="#" class="btn btn-default>Link styled as a button</a>
```
If clicking the button triggers a change on the page (but does not go to a different page), use a button.
```HTML
<button class="btn btn-default>Button that causes a change on the current page</button>
```

### Colours

#### Default / White
![Image of white bootstrap button](/images/whiteButton.jpg)
```HTML
<!-- Standard button style -->
<button type="button" class="btn btn-default">Default</button>
<a href="#" class="btn btn-default">Default</a>
```

#### Primary / Blue
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/primaryBlueButton.jpg)

```HTML
<!-- Identifies the primary action in a set of buttons -->
<button type="button" class="btn btn-primary">Primary</button>
<a href="#" class="btn btn-primary">Primary</a>
```
#### Success / Green
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/successGreenButton.jpg)

```HTML
<!-- Indicates a successful or positive action -->
<button type="button" class="btn btn-success">Success</button>
<a href="#" class="btn btn-success">Success</a>
```

#### Info / Grey
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/infoGreyButton.jpg)

```HTML
<!-- Contextual button for informational alert messages -->
<button type="button" class="btn btn-info">Info</button>
<a href="#" class="btn btn-info">Info</a>
```

#### Warning / Orange
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/warningOrangeButton.jpg)

```HTML
<!-- Indicates caution should be taken with this action -->
<button type="button" class="btn btn-warning">Warning</button>
<a href="#" class="btn btn-warning">Warning</a>
```

#### Danger / Red
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/dangerRedButton.jpg)

```HTML
<!-- Indicates a dangerous or potentially negative action -->
<button type="button" class="btn btn-danger">Danger</button>
<a href="#" class="btn btn-danger">Danger</a>
```

### Sizes

#### Large
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/largeButton.jpg)

```HTML
<!-- Large button: This can be done with any of the aforementioned colours  -->
<button type="button" class="btn btn-default btn-lg">Large</button>
<a href="#" class="btn btn-default btn-lg">Large</a>
```

#### Small
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/smallButton.jpg)

```HTML
<!-- Smallbutton: This can be done with any of the aforementioned colours  -->
<button type="button" class="btn btn-default btn-sm">Small</button>
<a href="#" class="btn btn-default btn-sm">Small</a>
```

#### Full Width
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/fullWidthButton.jpg)

```HTML
<!-- Full Width Button: This can be done with any of the aforementioned colours  -->
<button type="button" class="btn btn-default btn-block">Full-width button</button>
<a href="#" class="btn btn-default btn-block">Full-width button</a>
```

## Expanding and Collapsing Buttons
The following code snippets demonstrates a button toggle that will show or hide the section of text below it. Replace 'uniqueNameForControl' with a unique name for the code snippet. Every time you use this snippet on a page, you will need to provide a different 'uniqueNameForControl' for that particular code snippet (eg. uniqueName1, uniqueName2, uniqueName3, etc.)

```HTML
<h2><button aria-controls="uniqueNameForControl" aria-expanded="false" class="btn btn-primary" data-target="#uniqueNameForControl" data-toggle="collapse" type="button">More Info about Expandable Section</button></h2>
<div aria-expanded="false" class="collapse" id="uniqueNameForControl" role="region">
   <p>Content that will be shown or hidden using the button</p>
</div>

<h2><button aria-controls="uniqueNameForControl2" aria-expanded="false" class="btn btn-primary" data-target="#uniqueNameForControl2" data-toggle="collapse" type="button">More Info about Expandable Section</button></h2>
<div aria-expanded="false" class="collapse" id="uniqueNameForControl2" role="region">
   <p>Content that will be shown or hidden using the button</p>
</div>
```

# Images

### Shapes
#### Rounded Images
This demonstrates an image with rounded corners using the img-rounded class.
```HTML
<img src="/link/to/image" class="img-responsive img-rounded" />
```
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/roundedImage.jpg)

This demonstrates an image with rounded square corners and a border using the img-thumbnail class.
```HTML
<img src="/link/to/image" class="img-responsive img-thumbnail" />
```
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/thumbnailImage.jpg)

This demonstrates a circular image using the img-circle class.
```HTML
<img src="/link/to/image" class="img-responsive img-circle" />
```
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/circleImage.jpg)

### Aligning Images

####Centering Images
Avoid using ```<center>``` to center images on the page. Instead, use the "center-block" class.

```HTML
<img src="..." class="img-responsive center-block" alt="Descriptive alt text" />
```

####Floating Images Left
Use the "pull-left" or "pull-right" classes to float images left or right.
```HTML
<img src="..." class="img-responsive pull-left" alt="Descriptive alt text" />
```

####Floating Images Right

```HTML
<img src="..." class="img-responsive pull-right" alt="Descriptive alt text" />
```

####Clearing Floated Images
To clear a float, you can put a "clearfix" class on the parent element.

```HTML
<div class="clearfix"><img src="..." class="img-responsive pull-right" alt="Descriptive alt text" /></div>
```


### Creating a Responsive Image Grid

#### 2 Column Responsive Image Grid
Use the following code to create one row of a 2 column grid. Repeat for as many rows as you need. Remember to replace each img element with a decorative image that relates to the associated text link.

```HTML
<div class="row">
   <div class="col-md-6 col-lg-6 col-xs-12 col-sm-6">
      <figure class="thumbnail">
         <img alt="" class="img-responsive center-block img-rounded" src="/src/for/your/image" />
         <figcaption class="caption"><a href="#">Name of Link 1</a></figcaption>
      </figure>
   </div>

   <div class="col-md-6 col-lg-6 col-xs-12 col-sm-6">
      <figure class="thumbnail">
         <img alt="" class="img-responsive center-block img-rounded" src="/src/for/your/image" />
         <figcaption class="caption"><a href="#">Name of Link 2</a></figcaption>
      </figure>
   </div>
</div>
```
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/imageGrid.jpg)

#### 3 Column Responsive Image Grid
Use the following code to create one row of a 3 column grid. Repeat for as many rows as you need. Remember to replace each img element with a decorative image that relates to the associated text link.

```HTML
<div class="row">
   <div class="col-md-4 col-lg-4 col-xs-12 col-sm-4">
      <figure class="thumbnail">
         <img alt="" class="img-responsive center-block img-rounded" src="/src/for/your/image" />
         <figcaption class="caption"><a href="#">Name of Link 1</a></figcaption>
      </figure>
   </div>

   <div class="col-md-4 col-lg-4 col-xs-12 col-sm-4">
      <figure class="thumbnail">
         <img alt="" class="img-responsive center-block img-rounded" src="/src/for/your/image" />
         <figcaption class="caption"><a href="#">Name of Link 2</a></figcaption>
      </figure>
   </div>

   <div class="col-md-4 col-lg-4 col-xs-12 col-sm-4">
      <figure class="thumbnail">
         <img alt="" class="img-responsive center-block img-rounded" src="/src/for/your/image" />
         <figcaption class="caption"><a href="#">Name of Link 3</a></figcaption>
      </figure>
   </div>
</div>
```
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/imageGrid3.jpg)

#Slideshows
Use the following code to create an inline paginated slideshow.

```HTML
<div class="carousel slide" data-interval="false" data-keyboard="true" data-wrap="false" id="carousel-name">

	<div class="carousel-table">
		<a class="glyphicon glyphicon-chevron-left" data-slide="prev" href="#carousel-name" role="button"><span class="sr-only">Previous slide</span></a>

		<ul class="carousel-indicators pagination">
			<li class="active"><a data-slide-to="0" data-target="#carousel-name" href="#">1</a></li>
			<li><a data-slide-to="1" data-target="#carousel-name" href="#">2</a></li>
			<li><a data-slide-to="2" data-target="#carousel-name" href="#">3</a></li>
		</ul>
		<a class="glyphicon glyphicon-chevron-right" data-slide="next" href="#carousel-name" role="button"><span class="sr-only">Next slide</span></a>
	</div>

	<div class="carousel-inner" role="listbox">
		<div class="item active"><img alt="Alt text for first image. " class="img-responsive img-rounded" src="...">
			<h2>Heading for the first slide</h2>
			<p>Text for the first slide</p>
		</div>

		<div class="item"><img alt="Alt text for second image." class="img-responsive img-rounded" src="...">
			<h2>Heading for the second slide</h2>
			<p>Text for the second slide</p>
		</div>

		<div class="item"><img alt="Alt text for third image." class="img-responsive img-rounded" src="...">
			<h2>Heading for the third slide</h2>
			<p>Text for the third slide</p>
		</div>
	</div>
</div>
```
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/slideshow.jpg)

#Templates

##Two Columns
This code snippet demonstrates the method you would use to create two columns.

```HTML
<div class="row">
	<div class="col-sm-4">
		<ul>
			<li>Column 1 List Item 1</li>
			<li>Column 1 List Item 2</li>
			<li>Column 1 List Item 3</li>
		</ul>
	</div>

	<div class="col-sm-4">
		<ul>
			<li>Column 2 List Item 1</li>
			<li>Column 2 List Item 2</li>
			<li>Column 2 List Item 3</li>
		</ul>
	</div>
</div>
```
![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/twoColumn.jpg)

## Listing Text Content with a Left-Aligned Image
This code snippet demonstrates the method you would use to create a listing of content with a left-aligned image with text.

```HTML
 <div class="media-listing-page">
  <article class="row media">
    <div class="col-md-4">
      <div class="media-thumbnail"><img alt="" class="img-responsive img-rounded" src="image link"></div>
    </div>

    <div class="col-md-8">
      <header class="media-header">
        <h2 class="media-heading">heading</h2>
      </header>
  
      <div class="media-summary">
        <p>paragraph text</p>
       </div>
     </div>
  </article>
 </div>
```

### Notes:
- Add more "<article class='row media'>" tags to add new content
- Only need a single "media-listing-page" tag around all article tags
- You may need to use "Full HTML" mode before entering this HTML code. Note that only site managers have access to this mode.

![Image of all bootstrap buttons](/ccswbs/UoGd7-Training/blob/master/images/leftAllignedImage.jpg)