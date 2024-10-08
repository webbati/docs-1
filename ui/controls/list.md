---
title: "Controls: List"
---
# List

The list element is the base element of data viewing in Winter CMS. A list is made up of rows of data, similar to spreadsheet software like Excel, and contains columns of data. In general, the list is generally created by the [List Widget](/docs/v1.2/docs/backend/lists), but can also be manually created for custom uses.

## The basics

A list should be a standard `<table>` element with the classes of `table` and `data`. The table should contain a `<thead>` element with a single row that states the list column headings. The table itself should be wrapped with a `<div class="control-list">` element.

```html
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th class="sort-desc"><a>Title</a></th>
                <th class="active sort-asc"><a>Created</a></th>
                <th><span>Categories</span></th>
                <th><span>Updated</span></th>
                <th class="list-setup"><a title="List options"></a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Welcome to Winter</td>
                <td>Oct 01, 2013</td>
                <td>News</td>
                <td>Oct 01, 2013</td>
                <td>&nbsp;</td>
            </tr>
        </tbody>
    </table>
</div>
```

```backend
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th class="sort-desc"><a>Title</a></th>
                <th class="active sort-asc"><a>Created</a></th>
                <th><span>Categories</span></th>
                <th><span>Updated</span></th>
                <th class="list-setup"><a title="List options"></a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Welcome to Winter</td>
                <td>Oct 01, 2013</td>
                <td>News</td>
                <td>Oct 01, 2013</td>
                <td>&nbsp;</td>
            </tr>
        </tbody>
    </table>
</div>
```

### Complete example

```html
<div class="control-list">
    <table class="table data" data-control="rowlink">
        <thead>
            <tr>
                <th class="list-checkbox">
                    <div class="checkbox custom-checkbox nolabel">
                        <input type="checkbox" id="checkboxAll" />
                        <label for="checkboxAll"></label>
                    </div>
                </th>
                <th class="sort-desc"><a href="/">Title</a></th>
                <th class="active sort-asc"><a href="/">Created</a></th>
                <th class="sort-desc"><a href="/">Author</a></th>
                <th><span>Categories</span></th>
                <th><span>Published</span></th>
                <th><span>Updated</span></th>
                <th class="list-setup"><a href="/" title="List options"></a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_1" type="checkbox" />
                        <label for="checkbox_1">Check</label>
                    </div>
                </td>
                <td><a href="/">Welcome to Winter</a></td>
                <td>Oct 01, 2013</td>
                <td>Adam Person</td>
                <td>News</td>
                <td>Oct 01, 2013</td>
                <td>Oct 01, 2013</td>
                <td>&nbsp;</td>
            </tr>
            <tr class="active">
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_2" type="checkbox" checked="checked" /><label for="checkbox_2">Check The marketplace is open!</label>
                    </div>
                </td>
                <td><a href="/">The marketplace is open!</a></td>
                <td>Oct 15, 2013</td>
                <td>Sam Georges</td>
                <td>Features</td>
                <td>Oct 16, 2013</td>
                <td>Oct 16, 2013</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_3" type="checkbox" />
                        <label for="checkbox_3">Check Welcome to the Builder!</label>
                    </div>
                </td>
                <td><a href="/">Welcome to the Builder!</a></td>
                <td>Oct 21, 2013</td>
                <td>Alexey Bobkov</td>
                <td>News, Features</td>
                <td>Oct 21, 2013</td>
                <td>Oct 21, 2013</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_4" type="checkbox" />
                        <label for="checkbox_4">Check Components explained</label>
                    </div>
                </td>
                <td><a href="/">Components explained</a></td>
                <td>Nov 12, 2013</td>
                <td>Alexey Bobkov</td>
                <td>Tutorials</td>
                <td>Nov 12, 2013</td>
                <td>Nov 12, 2013</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_5" type="checkbox" />
                        <label for="checkbox_5">Check Creating a module in 90 seconds</label>
                    </div>
                </td>
                <td><a href="/">Creating a module in 90 seconds</a></td>
                <td>Nov 15, 2013</td>
                <td>Sam Georges</td>
                <td>Tutorials</td>
                <td>Nov 15, 2013</td>
                <td>Nov 15, 2013</td>
                <td>&nbsp;</td>
            </tr>
        </body>
    </table>
    <div class="list-footer">
        <div class="list-pagination">
            <div class="control-pagination">
                <span class="page-iteration">1-5 of 20</span>
                <a href="#" class="page-back" title="Previous page"></a><a href="#" class="page-next" title="Next page"></a>
            </div>
        </div>
    </div>
</div>
```

```backend
<div class="control-list">
    <table class="table data" data-control="rowlink">
        <thead>
            <tr>
                <th class="list-checkbox">
                    <div class="checkbox custom-checkbox nolabel">
                        <input type="checkbox" id="checkboxAll" />
                        <label for="checkboxAll"></label>
                    </div>
                </th>
                <th class="sort-desc"><a href="/">Title</a></th>
                <th class="active sort-asc"><a href="/">Created</a></th>
                <th class="sort-desc"><a href="/">Author</a></th>
                <th><span>Categories</span></th>
                <th><span>Published</span></th>
                <th><span>Updated</span></th>
                <th class="list-setup"><a href="/" title="List options"></a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_1" type="checkbox" />
                        <label for="checkbox_1">Check</label>
                    </div>
                </td>
                <td><a href="/">Welcome to Winter</a></td>
                <td>Oct 01, 2013</td>
                <td>Adam Person</td>
                <td>News</td>
                <td>Oct 01, 2013</td>
                <td>Oct 01, 2013</td>
                <td>&nbsp;</td>
            </tr>
            <tr class="active">
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_2" type="checkbox" checked="checked" /><label for="checkbox_2">Check The marketplace is open!</label>
                    </div>
                </td>
                <td><a href="/">The marketplace is open!</a></td>
                <td>Oct 15, 2013</td>
                <td>Sam Georges</td>
                <td>Features</td>
                <td>Oct 16, 2013</td>
                <td>Oct 16, 2013</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_3" type="checkbox" />
                        <label for="checkbox_3">Check Welcome to the Builder!</label>
                    </div>
                </td>
                <td><a href="/">Welcome to the Builder!</a></td>
                <td>Oct 21, 2013</td>
                <td>Alexey Bobkov</td>
                <td>News, Features</td>
                <td>Oct 21, 2013</td>
                <td>Oct 21, 2013</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_4" type="checkbox" />
                        <label for="checkbox_4">Check Components explained</label>
                    </div>
                </td>
                <td><a href="/">Components explained</a></td>
                <td>Nov 12, 2013</td>
                <td>Alexey Bobkov</td>
                <td>Tutorials</td>
                <td>Nov 12, 2013</td>
                <td>Nov 12, 2013</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td class="list-checkbox nolink">
                    <div class="checkbox custom-checkbox nolabel">
                        <input id="checkbox_5" type="checkbox" />
                        <label for="checkbox_5">Check Creating a module in 90 seconds</label>
                    </div>
                </td>
                <td><a href="/">Creating a module in 90 seconds</a></td>
                <td>Nov 15, 2013</td>
                <td>Sam Georges</td>
                <td>Tutorials</td>
                <td>Nov 15, 2013</td>
                <td>Nov 15, 2013</td>
                <td>&nbsp;</td>
            </tr>
        </body>
    </table>
    <div class="list-footer">
        <div class="list-pagination">
            <div class="control-pagination">
                <span class="page-iteration">1-5 of 20</span>
                <a href="#" class="page-back" title="Previous page"></a><a href="#" class="page-next" title="Next page"></a>
            </div>
        </div>
    </div>
</div>
```

### Empty list

Use the `no-data` class to display a list that contains no records.

```html
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th class="sort-desc"><a href="/">Title</a></th>
                <th class="active sort-asc"><a href="/">Created</a></th>
            </tr>
        </thead>
        <tbody>
            <tr class="no-data">
                <td colspan="100" class="nolink">
                    <p class="no-data">
                        There are no records in this view.
                    </p>
                </td>
            </tr>
        </tbody>
    </table>
</div>
```

```backend
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th class="sort-desc"><a href="/">Title</a></th>
                <th class="active sort-asc"><a href="/">Created</a></th>
            </tr>
        </thead>
        <tbody>
            <tr class="no-data">
                <td colspan="100" class="nolink">
                    <p class="no-data">
                        There are no records in this view.
                    </p>
                </td>
            </tr>
        </tbody>
    </table>
</div>
```

### Row classes

The following colored classes are available to use on the table row elements.

```html
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th class="sort-desc"><a href="/">Class</a></th>
            </tr>
        </thead>
        <tbody>
            <tr><td>Normal text</td></tr>
            <tr class="hidden"><td>.hidden</td></tr>
            <tr class="strike"><td>.strike</td></tr>
            <tr class="frozen"><td>.frozen</td></tr>
            <tr class="processing"><td>.processing</td></tr>
            <tr class="negative"><td>.negative</td></tr>
            <tr class="positive"><td>.positive</td></tr>
            <tr class="disabled"><td>.disabled / .deleted</td></tr>
            <tr class="new"><td>.new / .important</td></tr>
            <tr class="safe"><td>.safe / .special</td></tr>
        </tbody>
    </table>
</div>
```

```backend
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th class="sort-desc"><a href="/">Class</a></th>
            </tr>
        </thead>
        <tbody>
            <tr><td>Normal text</td></tr>
            <tr class="hidden"><td>.hidden</td></tr>
            <tr class="strike"><td>.strike</td></tr>
            <tr class="frozen"><td>.frozen</td></tr>
            <tr class="processing"><td>.processing</td></tr>
            <tr class="negative"><td>.negative</td></tr>
            <tr class="positive"><td>.positive</td></tr>
            <tr class="disabled"><td>.disabled / .deleted</td></tr>
            <tr class="new"><td>.new / .important</td></tr>
            <tr class="safe"><td>.safe / .special</td></tr>
        </tbody>
    </table>
</div>
```

### Status column

It might be fun to include a status column!

```html
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th style="width: 150px"><span>Status</span></th>
                <th class="active sort-asc"><a href="/">Title</a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>
                    <span class="wn-icon-circle text-muted">
                        Draft
                    </span>
                </td>
                <td>Welcome to Winter</td>
            </tr>
            <tr>
                <td>
                    <span class="wn-icon-circle text-info">
                        Pending
                    </span>
                </td>
                <td>What a wonderful day</td>
            </tr>
            <tr>
                <td>
                    <span class="wn-icon-circle text-success">
                        Approved
                    </span>
                </td>
                <td>The sun is shining</td>
            </tr>
            <tr>
                <td>
                    <span class="wn-icon-circle text-danger">
                        Cancelled
                    </span>
                </td>
                <td>The weather is sweet here</td>
            </tr>
        </tbody>
    </table>
</div>
```

```backend
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th style="width: 150px"><span>Status</span></th>
                <th class="active sort-asc"><a href="/">Title</a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>
                    <span class="wn-icon-circle text-muted">
                        Draft
                    </span>
                </td>
                <td>Welcome to Winter</td>
            </tr>
            <tr>
                <td>
                    <span class="wn-icon-circle text-info">
                        Pending
                    </span>
                </td>
                <td>What a wonderful day</td>
            </tr>
            <tr>
                <td>
                    <span class="wn-icon-circle text-success">
                        Approved
                    </span>
                </td>
                <td>The sun is shining</td>
            </tr>
            <tr>
                <td>
                    <span class="wn-icon-circle text-danger">
                        Cancelled
                    </span>
                </td>
                <td>The weather is sweet here</td>
            </tr>
        </tbody>
    </table>
</div>
```

### Badge column

You can also include an icon badge inside a column.

```html
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th style="width: 150px"><span>Status</span></th>
                <th class="active sort-asc"><a href="/">Title</a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>
                    <span class="list-badge badge-info">
                        <i class="icon-info"></i>
                    </span>
                    Draft
                </td>
                <td>Welcome to Winter</td>
            </tr>
            <tr>
                <td>
                    <span class="list-badge badge-warning">
                        <i class="icon-exclamation"></i>
                    </span>
                    Pending
                </td>
                <td>What a wonderful day</td>
            </tr>
            <tr>
                <td>
                    <span class="list-badge badge-success">
                        <i class="icon-check"></i>
                    </span>
                    Approved
                </td>
                <td>The sun is shining</td>
            </tr>
            <tr>
                <td>
                    <span class="list-badge badge-danger">
                        <i class="icon-times"></i>
                    </span>
                    Cancelled
                </td>
                <td>The weather is sweet here</td>
            </tr>
        </tbody>
    </table>
</div>
```

```backend
<div class="control-list">
    <table class="table data">
        <thead>
            <tr>
                <th style="width: 150px"><span>Status</span></th>
                <th class="active sort-asc"><a href="/">Title</a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>
                    <span class="list-badge badge-info">
                        <i class="icon-info"></i>
                    </span>
                    Draft
                </td>
                <td>Welcome to Winter</td>
            </tr>
            <tr>
                <td>
                    <span class="list-badge badge-warning">
                        <i class="icon-exclamation"></i>
                    </span>
                    Pending
                </td>
                <td>What a wonderful day</td>
            </tr>
            <tr>
                <td>
                    <span class="list-badge badge-success">
                        <i class="icon-check"></i>
                    </span>
                    Approved
                </td>
                <td>The sun is shining</td>
            </tr>
            <tr>
                <td>
                    <span class="list-badge badge-danger">
                        <i class="icon-times"></i>
                    </span>
                    Cancelled
                </td>
                <td>The weather is sweet here</td>
            </tr>
        </tbody>
    </table>
</div>
```

### Linking rows

You may link an entire row by adding the `data-control="rowlink"` attribute to the table element. The first table data (TD) column with an anchor will be used to link the entire row. To bypass this behavior, simply add the `nolink` class to the column.

```html
<div class="control-list">
    <table class="table data" data-control="rowlink">
        <tbody>
            <tr>
                <td>
                    <a href="http://wintercms.com">Link to this</a>
                </td>
                <td>Row will be linked</td>
                <td>This will also be linked</td>
                <td class="nolink">No link applied here</td>
            </tr>
        </tbody>
    </table>
</div>
```

```backend
<div class="control-list">
    <table class="table data" data-control="rowlink">
        <tbody>
            <tr>
                <td>
                    <a href="http://wintercms.com">Link to this</a>
                </td>
                <td>Row will be linked</td>
                <td>This will also be linked</td>
                <td class="nolink">No link applied here</td>
            </tr>
        </tbody>
    </table>
</div>
```

### Button column

You may add a small button to a list column by adding the `column-button` class to the table data (TD) element.

```html
<div class="control-list">
    <table class="table data" data-control="rowlink">
        <thead>
            <tr>
                <th style="width: 150px"><span>Action</span></th>
                <th><a href="javascript:;">Name</a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="column-button nolink">
                    <a
                        href="http://google.com"
                        target="_blank"
                        class="btn btn-secondary btn-sm">
                        Open Google
                    </a>
                </td>
                <td>
                    <a href="javascript:;">
                        Petoria
                    </a>
                </td>
            </tr>
        </tbody>
    </table>
</div>
```

```backend
<div class="control-list">
    <table class="table data" data-control="rowlink">
        <thead>
            <tr>
                <th style="width: 150px"><span>Action</span></th>
                <th><a href="javascript:;">Name</a></th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td class="column-button nolink">
                    <a
                        href="http://google.com"
                        target="_blank"
                        class="btn btn-secondary btn-sm">
                        Open Google
                    </a>
                </td>
                <td>
                    <a href="javascript:;">
                        Petoria
                    </a>
                </td>
            </tr>
        </tbody>
    </table>
</div>
```
