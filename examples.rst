.. Gloss Project documentation master file, created by
   sphinx-quickstart on Tue Nov 11 20:07:01 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. image:: gloss-logo.png


Howtos
=========================================

These are real world examples of using Gloss classes to solve real design/layout problems.

Content Assignment Examples
''''''''''''''''''''''''''''''''''''
These examples showcase some of the most common tasks done with Gloss

Adding a logo link and navigation menu
------------------------------------------
If your design has a logo surrounded by an anchor tag and want to magically put the actual site link::

    <a href=""><img src="pathtocoollogo.png" /></a>

Then use the `gl-logo` class like this::

   <a class="gl-logo" href=""><img src="pathtocoollogo.png" /></a>

Gloss will inject the correct home url into the href::

   <a class="gl-logo" href="http://home.example.com"><img src="pathtocoollogo.png" /></a>

  
Assigning a content area
---------------------------
It is common to have a main area where your most important content goes.
In this example we'll assume that that area has the id "main".
::

    <div id="main"> <!-- this is where main content goes --> </div>

Use the `gl-content` class like this::

    <div id="main" class="gl-content"> <!-- this is where main content goes --> </div>

Gloss will replace the content of 'main' with the content from your site::

    <div id="main" class="gl-content"> 
    content from my site
    <!-- this is where main content goes -->
    </div>


Adding the site edit-bar
---------------------------

Adding breadcrumbs
-------------------------

Adding a user menu
---------------------

Content Drop Examples
''''''''''''''''''''''''''''
Gloss provides drop classes which make it possible to remove/hide aspects of your layout that you don't want to be shown.
These can be removed everywhere, without exception, using the 'gl-drop' class or more selectively uing things like 'gl-front-drop'

Other Examples
''''''''''''''''''

Activating custom grids
---------------------------

Adding Custom CSS 
------------------------
Some times there is a need to override styles in place. It is always recommended that this be done within your HTML layout
however there are sometimes mitigating circumstances that prevent this. When faced with the need to quickly add CSS
you can make use of Gloss's `custom-css.xml` file.




