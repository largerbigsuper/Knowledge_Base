# git 使用


## git clone 避免输入密码


```shell

$ git clone https://<user>:<password>@<gitserver>/<path>/<repo>.git
```

当账号或密码中有特殊字符的时候需要进行替换，规则如下


```
!   #   $    &   '   (   )   *   +   ,   /   :   ;   =   ?   @   [   ]
%21 %23 %24 %26 %27 %28 %29 %2A %2B %2C %2F %3A %3B %3D %3F %40 %5B %5D
```

[GIT: Calling git clone using password with special character](https://fabianlee.org/2016/09/07/git-calling-git-clone-using-password-with-special-character/)