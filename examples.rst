.. Gloss Project documentation master file, originally created by
   sphinx-quickstart on Tue Nov 11 20:07:01 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. image:: gloss-logo.png


Howtos
=========================================

This collection of howtos aims to provide examples of using Gloss classes to solve real problems.

Content Assignment
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

  
Assigning a main content area
--------------------------------

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

The site edit-bar is usually available to site editors so that they can
quickly edit an article or other kind of content in context.
In this example we'll assign an edit bar to the part of the site with the id "main".
::

    <div id="main"> <!-- this is where main content goes --> </div>

Use the `gl-edit-bar` class like this::

    <div id="main" class="gl-edit-bar gl-content"> <!-- this is where main content goes --> </div>

Gloss will add the edit-bar to the beginning of the 'main' content for your site::

    <div id="main" class="gl-content gl-edit-bar">
    <edit-bar> <!-- the editbar ends up here --></edit-bar>
    content from my site
    <!-- this is where main content goes -->
    </div>
    
Adding breadcrumbs
-------------------------

The breadcrumbs are used to help a visitor know where they are within a website.
In this example we'll use a standalone div with an id of 'my-breadcrumbs' and assign breadcrumbs to
that div.
::

    <div id="my-breadcrumbs"> <!-- this is where breadcrumbs will go --> </div>

Use the `gl-breadcrumbs` class like this::

    <div id="my-breadcrumbs" class="gl-breadcrumbs"> <!-- this is where breadcrumbs will go --> </div>

Gloss will add the breadcrumbs to the beginning of the 'main' content for your site::

    <div id="my-breadcrumbs" class="gl-breadcrumbs">
    <breadcrumbs> <!-- the breadcrumbs end up here --></breadcrumbs>
    content from my site
    <!-- this is where breadcrumbs will go -->
    </div>
    
    
Adding a user menu
---------------------

The user menu provides quick access to a collection of personal and site configuration settings a visitor.
In this example we'll see how the user-menu can be quickly added to any div.
::

    <div id="my-menu"> <!-- this is where our menu will go --> </div>

Use the `gl-user-menu` class like this::

    <div id="my-menu" class="gl-user-menu"> <!-- this is where our menu will go --> </div>

Gloss will add the user-menu to the beginning of the div::

    <div id="my-menu" class="gl-user-menu">
    <user-menu> <!-- the breadcrumbs end up here --></user-menu>
    <!-- this is where our menu will go -->
    </div>
    
Layout Dropping
''''''''''''''''''''''''''''

Gloss provides `drop` classes which make it possible to remove parts of your layout as needed.
We call this procedure `layout dropping`. Layout can be removed everywhere, without exception, using the `gl-drop` class
or conditionally using classes like `gl-front-drop` and `gl-inner-drop`.

Dropping elements
---------------------------

The simplest example of layout dropping is removing something from everywhere on the site.
In this example we'll see how to use the `gl-drop` class to remove an unwanted element from our layout.
::

    <section> This is coolness
    <div id="annoying-item"> <!-- we want this to disappear --> </div>
   </section>
   
Use the `gl-drop` class like this::
  
    <section> This is coolness
    <div id="annoying-item" class="gl-drop"> <!-- we want this to disappear --> </div>
   </section>
   
Gloss will ensure that it doesn't show up in our layout::

   <section> This is coolness
    
   </section>

Dropping from the front page only 
---------------------------------------

.. note :: Gloss will only perform a front-drop on pages that are named `front-page`

To remove an element only from the front page we use the `gl-front-drop` class.
::

    <section> I am only meant to show up on inner pages
   </section>
   
Use the `gl-front-drop` class like this::
  
    <section class="gl-front-drop"> I am only meant to show up on inner pages
   </section>
   
Gloss will ensure that the element will be removed from the front page

Dropping from inner pages only 
---------------------------------------

.. note :: Gloss will only perform an inner-drop on pages that are NOT named `front-page`

To remove an element from inner pages we use the `gl-inner-drop` class.
::

    <section> I am meant to be dropped from inner pages
   </section>
   
Use the `gl-inner-drop` class like this::
  
    <section class="gl-inner-drop"> I am meant to be dropped from inner pages
   </section>
   
Gloss will ensure that the element will be removed from all inner pages

Dropping based on user role
------------------------------

The examples below illustrate the `gl-not-authenticated-drop` and `gl-not-manager-drop` classes.
They allow dropping based on absence of a role (in the case the authenticated and manager roles).

   <aside class="gl-not-authenticated-drop">
      This will not be visible to anonymous users
   </aside>  
   <aside class="gl-not-manager-drop">
      I will only be shown to a manager
   </aside>

Column based layouts
'''''''''''''''''''''''''

Adding markup to your layout to support column based layouts
-----------------------------------------------------------------

The underlying system dynamically supports two and three column layouts. Adding the following markup to your
layout will allow Gloss to tap into your own customizations.

.. note:: The `gl-left-sidebar` and `gl-right-sidebar` modifiers were introduced in version 0.6x of Gloss.
The older `gl-left-column` and `gl-right-column` can still be used but should be considered deprecated.

Two Columns (with left sidebar)

.. list-table::
   :widths: 25 75 
   :header-rows: 1

   * - I'm a left side bar
     - This is an example of a gl-two-column-layout gl-left-sidebar
     
.. list-table::
   :widths: 75 25 
   :header-rows: 1

   * - This is an example of a gl-two-column-layout gl-right-sidebar
     - I'm a right side bar
     
.. list-table::
   :widths: 25 50 25 
   :header-rows: 1

   * - I'm a left side bar
     - This is an example of a gl-three-column-layout
     - I'm a right side bar
     
     
     
Activating custom grids
---------------------------

Adding Custom CSS 
------------------------

If you need to add style related customizations make use of Gloss's `custom-css.xml` file.
Styles in `custom-css.xml` are given priority over styles provided by either the layout (theme)
or the source content.

To use it, go to the theming-controlpanel and select `modify theme`. Then look for the `custom-css.xml` file.


