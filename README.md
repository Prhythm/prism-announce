# \<prism-announce\>

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/Prhythm/prism-announce)

`<prism-announce>` is a [Polymer 2](http://polymer-project.org/) element provides simple yet fully customisable notifications.

# Usage

Place `<prism-announce>` in your application, and design how content message appears. Use `<prism-announce-toast>` and `<prism-announce-notification>` for toast and notification in material desgin.

```html
<prism-announce top right>
    <template>
        <style>
            .notification {
                background-color: #cfcfcf;
                border: 1px solid grey;
                padding: 7px;
                margin: 5px;
                display: flex;
                justify-content: space-between;
            }
        </style>
        <div class="notification">
            <span>Hello [[name]] at [[postTime]]</span> &nbsp;
            <button on-click="closeMessage">Close</button>
        </div>
    </template>
</prism-announce>
```
To announce a message, simply fire an `announce` event and assign content as a detail object. 

```javascript
element.dispatchEvent(new CustomEvent('announce', {
    bubbles: true,
    composed: true,
    detail: {
        name: this.name,
        postTime: new Date().toLocaleString()
    }
}))
```

# Styling

`<prism-announce>` provides the following custom properties and mixins for styling:

Custom property | Description | Default
----------------|-------------|----------
`--var-prism-announce` | Mixin applied to the element | `{}`

# Licence

MIT Licence