# chapter 11: Formatting Tables and Forms

* Using Tables the Right Way

```
<table>
    <caption align="bottom">
      Table 1: CosmoFarmer.com's Indoor Mower Roundup
    </caption>
    <colgroup>
      <col class="brand" />
      <col class="price" />
      <col class="power" />
    </colgroup>
    <thead>
      <tr>
        <th scope="col">Brand</th>
        <th scope="col">Price</th>
        <th scope="col">Power Source</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Chinook Push-o-matic Indoor Mower</td> <td>$247.00</td>
        <td>Mechanical</td>
      </tr>
      <tr>
        <td>Sampson Deluxe Apartment Mower</td>
        <td>$370.00</td>
        <td>Mechanical</td>
      </tr>
    </tbody>
</table>
```

Even with only three rows and three columns, the table uses nine unique HTML tags: `<table>, <caption>, <colgroup>, <col>, <thead>, <tbody>, <tr>, <th>, and <td>`. In general, more HTML isn’t a good thing, and you don’t need all of these tags: You can get away with just the `<table>, <tr>, and <td>` tags (and usually `<th>` as well). However, a table’s various tags give you lots of useful hooks to hang CSS styles on. The headers of each column—the `<th>` tags—can look different from other table cells if you create a `<th>` tag style, and you can use the `<colgroup>` tag as an easy way to set the width of a table column. This saves you the hassle of having to create lots of classes—like .tableHeader—and then apply them by hand to individual table cells. In the next section, you’ll see examples of how you can use these different tags to your advantage.

  ![t1](./t1.png)

* Styling Tables

Because tables are composed of several HTML tags, it helps to know which tag to apply a particular CSS property to. Applying padding to a `<table>` tag, for example, has no effect. The next few sections cover CSS properties for formatting tables and which HTML tags they get along with.

  * Adding Padding

  When it comes to tables, the borders are the edges of a cell, so padding adds space around any content you’ve placed inside of a table cell.

  You apply padding to either a table header or a table cell tag, but not to the `<table>` tag itself. So, to add 10 pixels of space to the inside of all table cells, use this style:
  ```
     td, th { padding: 10px; }

     td {
        padding-top: 10px;
        padding-right: 5px;
        padding-bottom: 3px;
        padding-left: 5px;
      }

      td {
        padding: 10px 5px 3px 5px;
      }
  ```

  * Adjusting Vertical and Horizontal Alignment

  To control where content is positioned within a table cell, use the `text-align` and `vertical-align` properties.

  Text-align controls horizontal positioning and can be set to left, right, center, and justify (see Figure 11-3). It’s an inherited property. (See Chapter 4 for more on inheritance.) When you want to right-align the contents of all table cells, create a style like this: ` table { text-align: right; }`

  This property comes in handy with `<th>` tags, since browsers usually center-align them. A simple style like `th { text-align: left; }` makes table headers align with table cells.

  ![t2](./t2.png)
