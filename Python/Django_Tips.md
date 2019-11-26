# Django Tips


## Admin Tips

### list all model fileds

```
list_display = [f.name for f in Book._meta.get_fields()]
```