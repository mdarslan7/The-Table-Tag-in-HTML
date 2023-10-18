# The `<table>` Tag in HTML

Tables! You've seen them everywhere—from Excel spreadsheets to data-heavy websites. Tables in HTML are a way of structuring data into rows and columns, giving them a tabular format. This structuring is done so that information can be easily interpreted from the tables.

This is how a basic HTML table looks like:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697631285097/698b5e12-3b97-48c9-b7e0-53165c1b240f.png)

In this article, let's explore how tables work and how can you create your own. Understanding the `<table>` tag and its child elements is essential for organizing and displaying tabular data on the web.

## `<table>` tag

First things first, the `<table>` tag serves as the foundation of your table. Think of it as the container for all the other table elements you'll learn about, just like your entire HTML gets wrapped up inside the `<html>` tag.

```html
<table>
  <!-- Table elements go here -->
</table>
```

## `<td>` tag

The smallest unit inside your table is the `<td>` tag which stands for 'table data'.

```xml
<td>Hi, I'm your first cell.</td>
<td>I'm your second cell.</td>
<td>I'm your third cell.</td>
<td>I'm your fourth cell.</td>
```

This code will create four 'table data' cells for you, and by default would place all the cells in the same line, in the same row, because we are not specifying the rows explicitly. Right now, they look like this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697632201138/d1246554-2c07-408d-b593-539f3afb5fda.png)

## `<tr>` tag

But that is not how we want our tables. We need to group our `<td>` tags to make an actual table and we do that by using `<tr>` tag which is 'table-row'. So if we copy our code multiple times and put them in `<tr>` tags, this is what we get.

```xml
<table>
        <tr>
            <td>Hi, I'm your first cell.</td>
            <td>I'm your second cell.</td>
            <td>I'm your third cell.</td>
            <td>I'm your fourth cell.</td>
        </tr>

        <tr>
            <td>Hi, I'm your first cell.</td>
            <td>I'm your second cell.</td>
            <td>I'm your third cell.</td>
            <td>I'm your fourth cell.</td>
        </tr>

        <tr>
            <td>Hi, I'm your first cell.</td>
            <td>I'm your second cell.</td>
            <td>I'm your third cell.</td>
            <td>I'm your fourth cell.</td>
        </tr>
</table>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697632466959/0ba71b6e-7394-412a-8dac-8d22febbb6c8.png)

For ease of understanding, we shall use some CSS in this tutorial, if you are familiar with borders and padding then well and good otherwise for now just paste this CSS into your HTML file, and you can explore this later.

```xml
<style>
    td {
        padding: 10px;
        border: 1px solid black;
    }
</style>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697632720606/d75e3262-4f32-4259-8e6b-2bec646b3907.png)

## `<th>` tag

Just like Thor our beloved God of Thunder is incomplete without his hammer, tables are incomplete without headers. Headers are bolded text above table columns that indicate what content is present inside each column, like **Full** **Name** -&gt; for Names. This is done using `<th>` 'table header' tag.

```xml
<tr>
       <th>First Col</th>
       <th>Second Col</th>
       <th>Third Col</th>
       <th>Fourth Col</th>
</tr>
```

Add a new row with three table headers in the existing code and you shall get this:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697633396344/6955b4fb-388d-40a2-8f81-81b75d9e1e11.png)

Notice how we have used four headers because there are four 'table data' cells in each row.

## `colspan` & `rowspan`

Sometimes we want our cells to span multiple rows and columns that is when we use `colspan` & `rowspan` attributes. They can be used with both `td` and `th` of course because both are types of table cells.

Consider the below example in which we have used both of these attributes.

```xml
<table>
        <tr>
            <th>First Col</th>
            <th>Second Col</th>
            <th>Third Col</th>
            <th>Fourth Col</th>
        </tr>
    
        <tr>
            <td rowspan="2">Hi, I'm your first cell.</td>
            <td colspan="2">I'm your second cell.</td>
            <td>I'm your fourth cell.</td>
        </tr>
    
        <tr>
            <td>I'm your third cell.</td>
        </tr>
    
        <tr>
            <td>Hi, I'm your first cell.</td>
            <td>I'm your second cell.</td>
            <td>I'm your third cell.</td>
            <td>I'm your fourth cell.</td>
        </tr>
</table>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697634136962/3448747c-a6bc-433f-a078-e43abfca73f7.png)

## `<colgroup>` & `<col>` tags

We covered a lot of stuff about rows in tables, columns should not feel left out. In tables, there is a way for us to define column groups and set attributes for columns. This is done using `<colgroup>` and `<col>` tags.

The `<col>` tag is used to apply attributes to individual table columns and is placed inside the `<colgroup>` tag. Whereas the `<colgroup>` tag is to group multiple `<col>` elements with similar attributes and is typically placed inside the `<table>` tag above any 'table rows'.

Let's consider an example where we shall use `<col>` to change the *background-color* of columns in our existing table.

```xml
<table>
        <colgroup>
            <col style="background-color: lightgray;">
            <col style="background-color: lightblue;">
            <col style="background-color: lightgreen;">
        </colgroup>
        <tr>
            <th>First Col</th>
            <th>Second Col</th>
            <th>Third Col</th>
            <th>Fourth Col</th>
        </tr>
    
        <tr>
            <td>Hi, I'm your first cell.</td>
            <td>I'm your second cell.</td>
            <td>I'm your third cell.</td>
            <td>I'm your fourth cell.</td>
        </tr>
    
        <tr>
            <td>Hi, I'm your first cell.</td>
            <td>I'm your second cell.</td>
            <td>I'm your third cell.</td>
            <td>I'm your fourth cell.</td>
        </tr>
    
        <tr>
            <td>Hi, I'm your first cell.</td>
            <td>I'm your second cell.</td>
            <td>I'm your third cell.</td>
            <td>I'm your fourth cell.</td>
        </tr>
</table>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697634930812/ea3caaab-dbc2-4ee9-a27f-37b9d61f1090.png)

Here you can see that only the first three columns have been colored because we used only 3 `<col>` tags.

## Table Structure

Lastly, we would cover how you can organize your table elements for better structure and styling. We use the following tags for table organization:

### 1\. `<thead>`

This section is used for column labels or headers. Anything you put here appears at the top of the table.

```xml
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>Email</th>
    </tr>
  </thead>
  <!-- More sections -->
</table>
```

### 2\. `<tbody>`

This contains the bulk of your data, it separates the header from the actual data, making the table structure more semantic.

```xml
<table>
  <!-- ... -->
  <tbody>
    <tr>
      <td>John</td>
      <td>30</td>
      <td>john@example.com</td>
    </tr>
  </tbody>
</table>
```

### 3\. `<tfoot>`

It can be used for summary information or any additional details related to the table data.

```xml
<table>
  <!-- ... -->
  <tfoot>
    <tr>
      <td colspan="2">Total People</td>
      <td>1</td>
    </tr>
  </tfoot>
</table>
```

Take a look at the below example where we have used these tags in our existing code for better readability & structure.

```xml
<table>
        <colgroup>
            <col style="background-color: lightgray;">
            <col style="background-color: lightblue;">
            <col style="background-color: lightgreen;">
        </colgroup>
        <thead>
            <tr>
                <th>First Col</th>
                <th>Second Col</th>
                <th>Third Col</th>
                <th>Fourth Col</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Hi, I'm your first cell.</td>
                <td>I'm your second cell.</td>
                <td>I'm your third cell.</td>
                <td>I'm your fourth cell.</td>
            </tr>
    
            <tr>
                <td>Hi, I'm your first cell.</td>
                <td>I'm your second cell.</td>
                <td>I'm your third cell.</td>
                <td>I'm your fourth cell.</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="4">This is the table footer.</td>
            </tr>
        </tfoot>
    </table>
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697635515957/32321fc9-39ff-488d-b44a-24e48dbc7b33.png)

And there you have it! You're now well-equipped to create tables in HTML. Refer to the below links for further reading.

* [https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)
    
* [https://www.tutorialspoint.com/html/html\_tables.htm](https://www.tutorialspoint.com/html/html_tables.htm)
    

Happy coding!
