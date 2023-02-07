# iconv-gbk

GBK 编码/解码

## 安装

```
$ npm i iconv-gbk
```

## 使用

此插件仅可运行在 Node 环境下，不支持浏览器环境。

```js
const { encodeGBK, decodeGBK } = require("iconv-gbk");

encodeGBK("测试文本");
//=> "%B2%E2%CA%D4%CE%C4%B1%BE"

decodeGBK("%B2%E2%CA%D4%CE%C4%B1%BE");
//=> "测试文本"
```

或者：

```js
const iconvGBK = require("iconv-gbk");

iconvGBK.encode("测试文本");
//=> "%B2%E2%CA%D4%CE%C4%B1%BE"

iconvGBK.decode("%B2%E2%CA%D4%CE%C4%B1%BE");
//=> "测试文本"
```

## API

### encodeGBK(text)

#### text

Type: `string`

### decodeGBK(str)

#### str

Type: `string`

## 优化

- 补充英文冒号编码不正确情况
- 补充空格编码不正确情况
- 去除编码字符前后空格

## 依赖

- [`iconv-lite`](https://github.com/ashtuchkin/iconv-lite)

## License

MIT © [zh-rocco](https://github.com/zh-rocco)
