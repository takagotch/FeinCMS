### feincms
---
http://www.feincms.org/

```py
from markdown2 import markdown
from feincms.module.models import Page
from django.db import models

class MarkdownPageContent(models.Model):
  context = models.TextField()
  
  class Meta:
    abstract = True
    
  def render(self, **kwargs):
    return markdown(self.context)
Page.create_content_type(MarkdownPageContent)
```

```
```

```
```


