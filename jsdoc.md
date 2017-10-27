```json
{
  "opts": { // JSDoc选项
    "template": "node_modules/minami", // 使用的主题模板
    "readme": "README.md", // 包含的readme文档
    "encoding": "utf8", // 输出的文档编码
    "tutorials": "./tutorials", // 包含的tutorial文档
    "destination": "./docs", // 输出地址
    "recurse": true, // 是否递归检索目录
    "verbose": true, // 
  },
  "source": { // 需要生成的注释的文件及目录
	"include": [ "./src" ], // 需要生成的
    "exclude": [], // 排除生成的
    "includePattern": ".+\\.js(doc)?$", // 匹配的格式
    "excludePattern": "(^|\\/|\\\\)_" // 排除的格式
  },
  "tags": {
    "allowUnknownTags": true, // 是否支持未知标签
    "dictionaries": [ // 使用的标签字典库
      "jsdoc" // 使用标准JSDoc标签字
    ]
  },
  "templates": { // 模板配置
    "cleverLinks": false, // 
    "monospaceLinks": false, // @link是否使用等宽字体
    "default": { // 默认配置
      "useLongnameInNav": true, // 是否使用长文件名
      "outputSourceFiles": true, // 是否在文档中导出源代码
      "includeDate": true, // 是否包含文档生成时间
      "staticFiles": {  // 静态资源输出到目标文件夹
        "include": [ // 包含的目录输出
          "./tutorials/assets"
        ],
        "exclude": [], // 排除的目录输出
        "includePattern": //, // 正则表达式，指明要复制的文件。如果这个属性没有被定义，所有的文件将被复制。
        "excludePattern": //, // 正则表达式，说明哪些文件跳过(不复制)。如果这个属性没有被定义，什么都不会被跳过。
      }
    }
  },
  "plugins": [
    "plugins/markdown" // 使用的插件
  ],
  "markdown": { // markdown插件的配置
    "hardwrap": true, // 使用硬换行
    "idInHeadings": true, // md标题使用ID
    "tags": [ // 支持md语法的标签
      "description",
      "param",
      "property",
      "returns",
      "throws",
      "todo",
      "example"
    ],
    "excludeTags": [ // 不支持md语法的标签
      "author",
      "classdesc",
      "see"
    ]
  },
  "docdash": { // docdash 模板自定义配置项
    "static": false, // 是否输出静态成员
    "sort": false // 是否对api名称进行排序
  }
}
```