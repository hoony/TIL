# Build

- Customize universal webpack config
    - edit `next.config.js`
    ```javascript
    module.exports = {
        webpack(config) {
            return config
        }
    }
    ```