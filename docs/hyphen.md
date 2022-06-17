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
                        "romanization": ["POJ","TL"]
                    }
                },
                {
                    "type": "atom",
                    "content": "雄",
                    "ruby": {
                        "content": "hiông",
                        "romanization": ["POJ","TL"]
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
                    "ruby": [{
                        "content": "chhī",
                        "romanization": ["POJ"]
                    },
                    {
                        "content": "tshī",
                        "romanization": ["TL"]
                    }
                    ]
                }
            ]
        }
    ]
}
```

When specify romanization="POJ", above code will render be like:

```
高雄市(Ko-hiông chhī)
```

And when specify romanization="TL", above code will render be like:

```
高雄市(Ko-hiông tshī)
```
