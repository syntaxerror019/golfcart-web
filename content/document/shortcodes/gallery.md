+++
title = 'Gallery'
date = 2026-06-12T00:00:00+00:00
draft = false
weight = 2
[params]
    author = 'GitHub Copilot'
+++


## Syntax

Use the `gallery` shortcode with a comma-separated list of image URLs, or provide one URL per line inside the shortcode body.

```markdown
{{</* gallery images="https://example.com/image1.jpg, https://example.com/image2.jpg, https://example.com/image3.jpg" */>}}
```

or

```markdown
{{</* gallery */>}}
https://example.com/image1.jpg
https://example.com/image2.jpg
https://example.com/image3.jpg
{{</* /gallery */>}}
```

## Render Style

```markdown
{{</* gallery */>}}
https://pic.imgdb.cn/item/63beb6b5be43e0d30e3aa660.jpg
https://pic.imgdb.cn/item/63beb6b5be43e0d30e3aa671.jpg
https://pic.imgdb.cn/item/63beb6b5be43e0d30e3aa684.jpg
{{</* /gallery */>}}
```

