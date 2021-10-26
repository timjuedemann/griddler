# Coldmine

Griddler is a SASS mixin that uses stepped CSS gradients to overlay any positioned element with a column grid of your choice. It probably makes the most sense to be used on the body element but it’s really up to you. 

Have any suggestions or feedback? [Reach out!](mailto:mail@timjuedemann.de)

## Installation
`npm install griddler` or if you're old-school download and import `griddler` ✌️

## Usage
Griddler currently consists of a single SASS mixin called `createGrid()` that accepts a total of 4 parameters.

**Template**

```scss
createGrid($cols, $gutter, $margin: null, $color: red);
```

**Test**

| Name | Description | Accepted values | Default |
|:---|---|---|---:|
| `$cols` | The number of columns the grid should consist of. | Unitless number| |
| `$gutter` | The gutter width separating the respective grid columns. | Any valid CSS unit | |
| `$margin` | The horizontal offset from the edges of the container that `createGrid()` is set on. | Any valid CSS unit | `0` |
| `$color` | The color the grid columns are displayed in. The default opacity is currently fixed to a value of `0.2` which seems like a sensible value for the majority of use cases. | Any valid CSS color | `red` |

Since the actual grid is based on an absolutely positioned `:after` pseudo element, `createGrid()` **must be set on a positioned element** in order to function properly.

**Example**

```scss
.container {
	width: 960px;
	margin: 0 auto;
	
	@include createGrid(12, 24px); // Creates a 12 column grid with a 24px gutter.
}
```


## Authors

* **Tim Jüdemann** - *Initial work* - [timjuedemann.de](http://timjuedemann.de/)

## License

This project is licensed under the MIT License.
