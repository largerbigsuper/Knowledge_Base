# centOS 常用命令


## 查看系统版本

`cat /etc/redhat-release`


```shell

[root@iZbp18ckbva4f17f7pxdqrZ ~]# cat /etc/redhat-release
CentOS Linux release 7.6.1810 (Core)

```

## 查看cpu信息

```shell

# 总核数 = 物理CPU个数 X 每颗物理CPU的核数 
# 总逻辑CPU数 = 物理CPU个数 X 每颗物理CPU的核数 X 超线程数

# 查看物理CPU个数
cat /proc/cpuinfo| grep "physical id"| sort| uniq| wc -l

# 查看每个物理CPU中core的个数(即核数)
cat /proc/cpuinfo| grep "cpu cores"| uniq

# 查看逻辑CPU的个数
cat /proc/cpuinfo| grep "processor"| wc -l


```