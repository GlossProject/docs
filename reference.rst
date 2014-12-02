.. Gloss Project documentation master file, created by
   sphinx-quickstart on Tue Nov 11 20:07:01 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. image:: gloss-logo.png


Reference
=========================================

The is the reference page for the Gloss web design process.

Gloss classes
---------------------


Core Classes
``````````````````````````````````````

Add these classes to your elements in the webflow interface. 

.. list-table::
   :widths: 20 80
   :header-rows: 1

   * - Class
     - Description
   * - <a>gl-logo
     - must be placed on a <a> tag, this is to preserve home link
   * - <nav>gl-menu
     - must be placed on a <nav> tag) marks the menu for replacement with the site's menu
   * - gl-menu-link
     - add style to individual menu items, very important if you want to control styles in your menu items.
   * - gl-edit-bar
     - adds an edit bar
   * - gl-content
     - assigns the site content
   * - gl-content-body
     - assigns ONLY the body of the content
   * - gl-content-byline
     - assigns ONLY the content byline
   * - gl-content-description
     - assigns ONLY the content description
   * - gl-content-title
     - assigns ONLY the content title
   * - gl-footer
     - assigns the footer
   * - gl-below-content
     - place additional content below the content

Drop Classes
``````````````````````````````````````

Use drop classes to remove unwanted elements

.. list-table::
   :widths: 20 80
   :header-rows: 1

   * - Class
     - Description
   * - gl-drop
     - drop elements marked with this class
   * - gl-front-drop
     - drop elements marked with this class if they are on the front-page
   * - gl-inner-drop
     - drop elements marked with this class if they are on an inner page.

Column and Side Bar Layout Classes
``````````````````````````````````````

Control dynamic site layout using the layout classes. It is for achieving layouts like:

.. list-table::
   :widths: 20 80
   :header-rows: 1

   * - Class
     - Description
   * - gl-one-column-layout
     - assign a content area that will (only be visible when there are no columns.)
   * - gl-two-column-layout gl-right-column
     - right column based layout
   * - gl-two-column-layout gl-left-column
     - left column based layout
   * - gl-three-column-layout
     - a layout containing a left and right column
   * - (gl-two-column-layout | gl-three-column) gl-first-column
     - used to assign which column is the first column in a two or three column layout
   * - (gl-two-column-layout | gl-three-column) gl-second-column
     - used to assign which column is the second column in a two or three column layout

Button and List Classes
``````````````````````````

These classes make it possible to style system buttons

.. list-table::
   :widths: 20 80
   :header-rows: 1

   * - Class
     - Description
   * - gl-button
     - a global that all buttons get  (they also get a bootstrap 3 .btn)
   * - gl-hot-button
     - a hot button, style it how you like and it will get that style wherever hot buttons show up in your site. (also includes a bootstrap 3 .btn-danger)
   * - gl-cool-button
     - a cool button, style it how you like and it will get that style wherever cool buttons show up in your site. (also includes a bootstrap 3 .btn-primary)
   * - gl-cooler-button
     - a cooler button  (also includes a bootstrap 3 .btn-info)
   * - gl-default-button
     - a default style applied to all other buttons (also includes a bootstrap 3 .btn-default)
   * - gl-ul
     - Used for styling unordered lists
   * - gl-ol
     - Used for styling ordered lists
   * - gl-ul-li
     - Used for styling unordered list items
   * - gl-ol-li
     - Used for styling ordered list items
