# hyphen

对于一些语言的拉丁化存在连字符的情况，可以设置开启hyphen来满足一个phrase内多个atom之间会连字。本key为optional的。

例子：

```json
{
    "hierarchy": "sentence",
    "meta": {
        "language": "zh-nan",
    },
    "content": [
        {
            "type": "phrase",
            "hyphen": "true",
            "content": [
                {
                    "type": "atom",
                    "content": "高",
                    "ruby": {
                        "content": "Ko",
                        "romanization": "POJ"
                    }
                },
                {
                    "type": "atom",
                    "content": "雄",
                    "ruby": {
                        "content": "hiông",
                        "romanization": "POJ"
                    }
                },
            ]
        },
        {
            "type": "phrase",
            "hyphen": "false",
            "content": [
                {
                    "type": "atom",
                    "content": "市",
                    "ruby": {
                        "content": "chhī",
                        "romanization": "POJ"
                    }
                }
            ]
        }
    ]
}
```

Will render be like:

```
高雄市(Ko-hiông chhī)
```
