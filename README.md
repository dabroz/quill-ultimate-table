# quill-ultimate-table

<p>
  <a href="https://www.npmjs.com/package/quill-ultimate-table"><img src="https://img.shields.io/npm/v/quill-ultimate-table.svg?sanitize=true" alt="Version"></a>
  <a href="https://npmcharts.com/compare/quill-ultimate-table?minimal=true"><img src="https://img.shields.io/npm/dm/quill-ultimate-table.svg?sanitize=true" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/quill-ultimate-table"><img src="https://img.shields.io/npm/l/quill-ultimate-table.svg?sanitize=true" alt="License"></a>
</p>

> Note: This is the ultimate version of the `quill-better-table` npm package, including changes from
> `quill-better-table-plus`.

# Summary

`quill-ultimate-table` is an enhanced version of the `Quill` rich text editor plugin that provides more powerful and
flexible table editing features.It enables users to easily create, edit and format tables, as well as perform more
complex table operations.

This package is an enhancement based on the latest available version of the original `quill-better-table` package,
adding a number of new features and fixing a number of known issues to ensure that it is suitable for current
environments and needs.

## requirement

[quilljs](https://github.com/quilljs/quill) v2.0.0+

<!-- TODO
## Online Demo

[quill-ultimate-table Codepen Demo](https://codepen.io/seehar/pen/yLQopvq)
-->

# Install

You can install `quill-ultimate-table` via npm:

```shell
npm install quill-ultimate-table
```

# Use

Import `Quill` and style dependencies

```html

<script src="https://cdnjs.cloudflare.com/ajax/libs/quill/2.0.0/quill.min.js" type="text/javascript"></script>
```

```html

<link href="https://cdnjs.cloudflare.com/ajax/libs/quill/2.0.0/quill.snow.min.css" rel="stylesheet">
<link href="https://unpkg.com/quill-ultimate-table@1.0.0/dist/quill-ultimate-table.css" rel="stylesheet">
```

## ES6

```javascript
import QuillUltimateTable from 'quill-ultimate-table'

Quill.register({
  'modules/ultimate-table': QuillUltimateTable
}, true)

window.onload = () => {
  const quill = new Quill('#editor-wrapper', {
    theme: 'snow',
    modules: {
      table: false,  // disable table module
      'ultimate-table': {
        operationMenu: {
          items: {
            unmergeCells: {
              text: 'Another unmerge cells name'
            }
          }
        }
      },
      keyboard: {
        bindings: QuillUltimateTable.keyboardBindings
      }
    }
  })

  document.body.querySelector('#insert-table')
    .onclick = () => {
    let tableModule = quill.getModule('better-table-plus')
    tableModule.insertTable(3, 3)
  }
}
```

<!-- TODO
# Future Functions

We plan to further enhance `quill-ultimate-table` by adding the following features in a future release:

- [ ] **Adapts to multiple `table` formats**: Supports a wide range of directly copied and pasted `table` data with
  styles and better parsing and rendering.
- [ ] **Expose more `api`**: Provide more `api` for developers to use in order to quickly apply different features,
  looks and styles.
- [ ] **`Typescript` support**

We are working hard on these features and will gradually roll them out in future releases. Stay tuned!

If you have any other feature suggestions or ideas, feel free to raise them in the issue, we'd love to hear your
feedback and contributions.
-->
# Community

Feel free to contribute code and submit issues. If you find any bugs, or have suggestions for improvements, please
create an issue or submit a pull request.

# License

[MIT License](https://rmm5t.mit-license.org/)
