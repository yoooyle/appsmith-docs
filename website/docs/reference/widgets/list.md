# List

You can use a list widget to display structured data collection. For example, You have a dataset of employees with each entity having properties like name, designation, department, etc. You can use a list widget to iterate over the employee collection and display the data one after the other. The list widget allows you to supply this dataset and takes care of the iteration without writing any code.

:::info
List widget is in beta right now. It can only render widgets for display purposes like text, images, etc., in the template, but we plan to offer more features in the future.
:::

<figure>
  <object data="https://www.youtube.com/embed/0ePiZlWmp7Q?autoplay=0" width='860px' height='515px'></object> 
  <figcaption align="center"><i>How to use List Widget</i></figcaption>
</figure>

## Usage

List widget provides you with out-of-the-box functionality to iterate over a structured data collection. The datasets can be static or generated by the response from API/queries.

A list widget will help you better visualize your content. You can use rich content to display in a list widget like you can add images, text, buttons, audio, and more.

Below are some use cases where a list widget could help display data:

* Display information about your business, such as customer reviews, purchase orders, store locations, etc.
* You can show book details like title, cover image, genre, author, publication date, and price.
* Display employees' information. You can keep track of employee history, birthdays, and more.

These were just a few examples, and you can do several things with the list widget. The image below depicts how employee data will appear in the list widget: an employee's picture, personal details (email, date of birth), employee ID, department, city, and a button `View Details` that displays more details like the date of joining, address, and account details.

![A simulation to display an employee's information using a list widget](/img/employedatass1.PNG)

## Add to Canvas

To add a list widget to your canvas, drag a list widget from a widget pane available on the left navigation bar.

Navigate to PAGES —> Select Widget Tab —> Write “**list”** in the search bar —> Drag the widget on the canvas.

<figure>
  <object data="https://www.youtube.com/embed/8LWM10svhZU?autoplay=0" width='860px' height='515px'></object> 
  <figcaption align="center"><i>Add a widget to Canvas</i></figcaption>
</figure>


Now that you have a list widget added to the canvas, you can move it anywhere on the canvas by simply dragging the widget.

## Components

Typically, a list widget is a collection of other widgets that you can embed to display data. Once you drag the list widget on the canvas, you can see it has embedded widgets like an[ image](https://docs.appsmith.com/widget-reference/image) and two[ texts](https://docs.appsmith.com/widget-reference/text) available.

![Child widgets embedded in a list widget](/img/List-Widget-Embedded-Widgets.png)

For example, you are building an employee directory and want to display the name, image, designation, and department. You can use the below components to display the employee data in a list widget:

* Text widget - to display employee name.
* Image widget - to show employee’s picture.
* Text widget - to populate designation.
* Text widget - to display department.

So, your list widget will be a collection of three text widgets and one image widget.

The platform provides a list widget with an embedded image and two text widgets. You can add more widgets as per your requirement.

:::info
In the beta version of the List widget, you can only use widgets to display the data like images, text, and more. However, the widgets that need users to provide inputs like text box, checkbox, and more, are not available in beta but will be added as part of future releases.
:::

To add more widgets to your list, navigate to the left bar under **PAGES**, click on the **Widget** tab, and search for a widget like **Text**. **Drag** the widget on the first item for the list in the widget.

![](</img/List-Widget-Add-widgets-to-first-item_(1).png>)

:::tip
Add the widgets only on the first item container in the list. The widgets will be replicated for the other items whenever the data renders automatically. We’ll learn more about how the embedded widgets replicate on a dataset in the subsequent section below.
:::

The next thing you would like to do is set up some data for the list widget. You can do that by configuring properties for the widget.

## Properties

Properties allow you to edit the widget, connect it with other widgets and customize the user actions.

### Widget Properties

These properties allow you to name, edit the List widget.

#### Name of Widget

You can see a textbox available at the top of the Properties pane. List1 is the default name given to a list widget added to the canvas. The number `{1}` in List1 is a running sequence. If you add more list widgets, the names of the subsequent list widgets could be like List2, List3, and more.


<figure>
  <object data="https://www.youtube.com/embed/WqSrZphpZv4?autoplay=0" width='860px' height='515px'></object> 
  <figcaption align="center"><i>How to name a list widget?</i></figcaption>
</figure>

:::info
It’s advisable to rename the widget to give some meaningful name. It makes it easy to pass parameters by using the widget name to the APIs or queries.
:::

All of these properties are present in the property pane of the widget. The following table lists all the widget properties.

| Property                   | Description                                                                                                                                                                                                                                               |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Items**                  | Allows you to bind static or dynamic data collection to the widget.                                                                                                                                                                                       |
| **Server-side Pagination** | Enables you to implement pagination by limiting the number of results fetched per API / Query request. [See here](../../core-concepts/data-access-and-binding/displaying-data-read/display-data-tables.md#pagination) for more information on pagination. |
| **Visible**                | Controls widget's visibility on the page. When turned off: The widget will not be visible when the app is published. It appears translucent when in Edit mode.                                                                                            |
| **Animate Loading**        | When turned off, the widget will load without any skeletal animation. You can use a toggle switch to turn it on/off. You can also turn it off/on using javascript by enabling the JS label next to it.                                                    |

#### Items

Items are used to bind your dataset with the list widget. Either you want to iterate over static or dynamic data generated by executing a database Query/API call.

To have a dynamic data binding for the list widget, you can use the **Connect Data** button on the right bar or choose the Queries/API/JS functions from the left navigation bar available under the **Explorer** tab.


<figure>
  <object data="https://www.youtube.com/embed/PPsqqkaq_7Q?autoplay=0" width='860px' height='515px'></object> 
  <figcaption align="center"><i>How to add Data to Widget?</i></figcaption>
</figure>

#### Connect Data

When you click on the **Connect Data** button, it navigates to the DataSources page, where you can either add new datasources or choose existing datasources. On the datasources page, once you have selected the datasource, you can either add queries or select available queries to bind the response to the list widget.[ Read more to add different datasources and create queries.](../../core-concepts/connecting-to-data-sources/)

#### Explorer Tab

On the **Explorer** tab, you’ll have options to choose from Queries to Javascript(JS) functions to datasources and queries. Choose one of the options that would enable you to add data to the list widget.

#### Data Mapping

You can see a box displaying the static JSON data. You can replace the static JSON in the items pane or bind the query/API/JS response, and the list widget will use the data for generating the items.

If you wish to bind the dynamic response of the queries/API, then you can use mustache syntax (`{{ }}`) to embed the same. For example, You have written a query `“GetAllEmployees”` then to bind the response use `{{GetAllEmployees.data}}`. Typically, you will have a format of `{{QUERY_NAME.data}}` to bind the data returned by the query.

To better understand how to bind data to a list widget, let’s take an example of static Javascript Object Notation (JSON).

You’ll see that in the JSON snippet below, there is a collection of books with details like `bookId`, `bookName`, `bookImage`, `category`, `author`, `publishedDate`, and `price`.

```
[

  {

    "bookId": "001",

    "bookName": "Artificial Intelligence for Business Leaders",

    "bookImage": "https://m.media-amazon.com/images/I/511Y1LSr0JL.jpg",

    "category":"Computing, Internet & Digital Media",

    "author" :"Ajit K Jha",

    "publishedDate": "22-July-2020",

    "price": "INR 599"

  },

  {

    "bookId": "002",

    "bookName": "Bootstrap 4 Quick Start",

    "bookImage": "https://images-na.ssl-images-amazon.com/images/I/41GTBaVKAyL._SX404_BO1,204,203,200_.jpg",

    "category":"Computing, Internet & Digital Media",

    "author" :"Jacob Lett",

    "publishedDate": "20-March-2018",

    "price": "INR 439.90”

 }

]
```

Replace the above JSON snippet in the items pane. To display the data in the list widget, you’ll need five text widgets and one image widget. Drag and drop these widgets on the canvas, and remember to add the widgets on the **first item** of the list widget. You’ll see that the items will simulate iteration so that you can visualize iterated data.

Let’s bind each JSON field to the widgets embedded in the list widget. You can follow similar steps to bind the data for other widgets:

* Select the Image widget.
* In the right bar for General Properties, input the code snippet `{{currentItem.bookImage}}`. Please note that `currentItem` refers to the item read from the data collection. It is similar to the iterator reference of the collection you would be iterating over in the code. `bookImage` is the JSON attribute in the above code snippet.
* You will see that the image is now displayed, as the image widget renders the image available on the URL supplied in JSON.

Similarly, you can bind bookName, category, author, publishedDate, and price to the embedded widgets in the list widget. Once you link the data, you can see that the list widget will display the data for the JSON.

:::info
If you are binding the dynamic response of your query or API to the list widget, remember to use the query columns or API response object’s attributes to map to the individual widget by using `currentItem.<attribute_or_column_name>`.
:::

#### Server Side Pagination

You can use server-side pagination when a client receives only a subset of data from large datasets. It allows you to define the data limit that a Query or an API call can render. Thus, allowing you to paginate the data and determine the pagination boundaries.[ Read more on server-side pagination to paginate your large data sets](../../core-concepts/data-access-and-binding/displaying-data-read/display-data-tables.md).

#### Visible

You can use Visible to show or hide the widget. By default, visible is **on** that is enabled, so the widget is visible on page load. This property particularly comes in handy when you want to **hide/show** a widget programmatically or hide a widget on page load and then show it when a particular condition or data is available.

There are two ways in which you can manipulate this property.

* Enable the JS label next to Visible and write the javascript code that can handle the show and hide of the widget by manipulating visible property.
* Write your own JS object and javascript code to link to any other widget and manage the show/hide.

:::tip
You can get the reference of visible property by using `{{widget_name.isVisible}}` in your code.
:::

For example, let’s drag a checkbox widget `Checkbox1` onto the canvas and bind it to the `Visible` property of the list widget by enabling the JS label next to it, add the following JavaScript code in the `Visible` property of the list widget.

```
{{Checkbox1.isChecked}}
```

When you check the checkbox, it will enable the Visible property, and shows the list widget. Whereas the uncheck on the checkbox will hide the widget.

{% embed url="https://youtu.be/iJICPdtoUQc" %}
<figure>
  <object data="https://www.youtube.com/embed/iJICPdtoUQc?autoplay=0" width='860px' height='515px'></object> 
  <figcaption align="center"><i>Visible</i></figcaption>
</figure>


### Binding Properties

These properties allow you to bind your List widget with any other widget in queries or JS objects. The following table lists all the binding properties.

| Binding Property    | Description                                                                                                                                                                                                                               |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **backgroundColor** | Represents the widget's **Background Color** setting as a CSS `color` value _(string)_.                                                                                                                                                   |
| **gridGap**         | Reflects the widget's **Item Spacing** property _(number)_.                                                                                                                                                                               |
| **isVisible**       | Reflects the state of the widget's **Visible** setting _(bool)_.                                                                                                                                                                          |
| **items**           | Contains an *array* of *objects* that each represent a widget within the list items, and holds information about that widget's state.<br/>e.g. `[ { "Text1": { "isVisible": true, ... }, ... }, ... ]` |
| **listData**        | Contains an _array_ of _objects_ that each represent a list item and its data.                                                                                                                                                            |
| **pageNo**          | Contains a _number_ representing which page of the list is currently being displayed.                                                                                                                                                     |
| **pageSize**        | Contains a _number_ representing the number of list items that can fit on one page of the List widget.                                                                                                                                    |
| **selectedItem**    | Contains an _object_ representing the data of the list item that is selected.                                                                                                                                                             |

### Events

You can define functions that will be called when these events are triggered in the widget.

| Event               | Description                                                                                                                                                                                                                                             |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **onListItemClick** | Sets an action to take place when the user clicks on one of the list items. Can be set from the GUI list of common actions ([examples here](../appsmith-framework/widget-actions/)), or you can define a custom JavaScript function to call instead. |

#### onListItemClick

For a list widget, the event onListItemClick is fired whenever a user clicks or selects an item on the list. You can perform many[ supported actions](../appsmith-framework/widget-actions/) on a list item click.

For example, show a message whenever a user clicks on a list item.

:::info
An individual item on the list is defined as the entire row. A row includes the widgets embedded into it. You can get the values of embedded widgets for the selected or clicked item in your code to perform various operations.
:::

<figure>
  <object data="https://www.youtube.com/embed/_h3hUjnGwSE?autoplay=0" width='860px' height='515px'></object> 
  <figcaption align="center"><i>onListItemClick</i></figcaption>
</figure>


### Styles

You can do some formatting changes to enhance the look and feel of the widget by using styles.

| Style Property            | Description                                                                                                                                                                      |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Background Color**      | Sets the background color of the widget. Accepts  CSS [`color` ](https://developer.mozilla.org/en-US/docs/Web/CSS/color)values.                                                  |
| **Item Background Color** | Sets the background color of the list item cards. Accepts  CSS [`color` ](https://developer.mozilla.org/en-US/docs/Web/CSS/color)values.                                         |
| **Item Spacing**          | Sets the width in pixels of the gap between list item cards. Accepts _number_ values.                                                                                            |
| **Border Radius**         | Rounds the corners of the widget's outer edge. With JS enabled, this accepts valid CSS [`border-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius) values. |
| **Box Shadow**            | Casts a drop shadow from the frame of the widget. With JS enabled, this accepts valid CSS [`box-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow) values.    |

#### Background Color

You can use the property background color to change the widget’s background. You can select the available colors from the color pallet to change the background color.

#### Item Background Color

Like Background color, you can select the available colors from the pallet to change the item’s background color for your widget.

![How to set background/item background color for a list widget?](/img/List-Widget-Background-Item-Background-Color.png)

:::tip
To change the background/item background color by using HTML Color codes, click the JS label next to Background Color/ Item Background Color label and supply the HTML Color code in the box below.
:::

#### Item Spacing

You can use item spacing to add the padding to the list cells. Padding will ensure that you have some space included between the adjacent cells of the widget. Item spacing uses Pixels(px) as a unit. You can supply a number like 5 to the item spacing that adds the padding of 5px to the list cells.

#### Border Radius

You can use the border radius style to curve the edges of list widget. You can select one of the available option to choose the border radius.

#### Box Shadow

You can use the box shadow style to cast a drop shadow of list widget. You can select one of the available option to choose the box shadow.

Take advantage of using the list widget to display your datasets and visualize your content in a better way.