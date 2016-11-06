# chapter 16 : Using a CSS Grid System

* Structuring Your HTML for Grids

Individual web designers—and big companies like Twitter—have created dozens of CSS grid systems to choose from.T hese systems rely on one or more CSS files designed to create the kind of columns described in the previous section. Most of these systems use a similar approach for structuring the HTML to create a grid, relying on a series of nested `<div>` tags to form three different types of page elements:

  * Containers - A container div holds one or more rows.The container helps set a width for the entire grid system, and often uses the max-width property (page 208) to keep the content from growing absurdly wide on large monitors. Containers are also usually centered in the middle of the browser window.

  * Rows - A row is another `<div>` tag,placed within a container,and the row holds more divs that make up the columns within it.

  * Columns - A column is a `<div>` tag within a row. Each row has one or more columns.
