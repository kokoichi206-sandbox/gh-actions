## ローカルで openapi の確認

``` sh
make bootstrap
make preview
```

## Stub server の起動

[prism](https://github.com/stoplightio/prism) を使うことで stub server を立てることが可能です。

``` sh
# デフォルトでは 127.0.0.1:4010 で起動する。
$ prism mock openapi.yml

# port を指定する。
$ prism mock openapi.yml -p 2828
```
