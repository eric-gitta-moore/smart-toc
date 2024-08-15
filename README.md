# Simple Outliner / 智能网页大纲 (for Chrome), 💥 Support Inoreader and Feedly

> Simple Outliner / 自动生成网页大纲、目录，Support Inoreader and Feedly。

## Download

- Chrome extension: [Simple Outliner / 智能网页大纲](https://chrome.google.com/webstore/detail/smart-toc-%E6%99%BA%E8%83%BD%E7%BD%91%E9%A1%B5%E5%A4%A7%E7%BA%B2/ppdjhggfcaenclmimmdigbcglfoklgaf)

## Build

Requires `node.js` and `yarn`

```bash
# install dependencies
yarn

# build and bundle the extension as `.zip` for release
yarn run build

# build/watch the extension for local development (please use Chrome's `Load unpacked extension` to load `/dist` folder)
yarn run start
```

Thank you for using the extension. Any suggestions/issues/problems are welcomed!

## 直接引入网页使用
```html
<script>
window.chrome = {
    runtime: {
        sendMessage() { },
        onMessage: {
            addListener() { }
        }
    },
    storage: {
        local: {
            get(options, callback) { callback({ autoType: '1' }) },
            set() { }
        }
    }
}
</script>
<script src="https://raw.githubusercontent.com/eric-gitta-moore/smart-toc/resource/dist/toc.js"></script>
```