## 1-创建vue.config.js

`vue.config.js`配置别名

```javascript
module.exports = {
    configureWebpack:{
        resolve:{
            //别名
            alias:{
                'assets':'@/assets',
                'common':'@/common',
                'components':'@/components',
                'network':'@/network',
                'views':'@/views'
            }
        }
    }
}
```

## 2-.editorconfig配置相关文件

```
root = true

[*]
charset = utf-8
indent_style = space
indent_size = 2
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true
```

