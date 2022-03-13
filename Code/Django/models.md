# Models

The relations for the database are defined here

<https://docs.djangoproject.com/en/3.2/topics/db/models/>

Imports

from django.db import models
from django.db.models.deletion import SET_NULL

Example Item:

```python
class Item(models.Model):
    name = models.CharField(max_length=45)
    categorie = models.ForeignKey(
        Categorie, on_delete=models.SET_NULL, null=True)

    def __str__(self) -> str:
        return self.name

    class Meta:
        ordering = ["name"]
```

## Relationfields

### Foreignkey, Many-to-one relationships

categorie = models.ForeignKey(Categorie, on_delete=models.SET_NULL, null=True)

### Many-to-many relationships

item = models.ManyToManyField(Item, related_name='items', blank=True)

### OneToOneField, One-to-one relationships

...
