# Django RestFrameWork


## 请求构造流程

```shell
self.perform_authentication(request)
self.check_permissions(request)
self.check_throttles(request)
```