# 一些有关词汇

## 猫码

CatCode（猫码） 是 PolarCore 中的约定。它本身是一个占位符，用于表达特殊信息
例如：`What is that?[Image:(Base64)https://an.url/to/image.png][At:UserID]' 目前猫码支持以下通用格式：

[Image:URL(Base64)/ImageID]

[At:UserID]

[AtAll]

[Plain:Text] (纯文本，通常不需要手动指定格式)

所有Wrappers应当实现猫码标准。

### *开发小课堂
猫码中的链接需要Base64加密，如下

```java
String baseURL = Image
    .builder()
    .URI("https://an.url/to/image.png")
    .build()
```