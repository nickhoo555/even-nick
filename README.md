# 修改 hugo 主题 even

## 新增字体
### webpack 配置

```js
{
  test: /HYYouYuanTiW\.(woff|eot|ttf|otf|svg)$/,
  use: ['file-loader?name=[path][name].[ext]']
}
```

### 定义字体

参照 `src/css/_variables.scss`，自定义 `src/css/_custom/_custom.scss`
```scss
// 已通过 fontmin 精简字体文件
// Font family: yyt
@font-face {
    font-family: 'yyt';
    src: url('../fonts/yyt/HYYouYuanTiW.eot');
    src: local('yyt'), url('../fonts/yyt/HYYouYuanTiW.eot?#iefix') format('embedded-opentype'),
    // url('../fonts/yyt/HYYouYuanTiW.woff2') format('woff2'),
    url('../fonts/yyt/HYYouYuanTiW.woff') format('woff'),
    url('../fonts/yyt/HYYouYuanTiW.ttf') format('truetype'),
    url('../fonts/yyt/HYYouYuanTiW.svg#apple-chancery') format('svg');
    font-weight: lighter;
    font-style: normal;
  }
```
## 修改logo字体

```scss
// Font family of the logo.
$logo-font-family: 'yyt', sans-serif !default;
```

## 修改菜单字体
`src/css/_partial/_header/_menu.scss` 
## 构建 `yarn build`