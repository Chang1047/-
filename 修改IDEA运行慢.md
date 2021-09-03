# 修改IDEA运行慢

在IDEA安装目录中找到<font color='red'>idea64.exe.vmoptions</font>

原本内容为

```java
-Xms128m
-Xmx750m
-XX:ReservedCodeCacheSize=512m
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=50
-XX:CICompilerCount=2
-XX:+HeapDumpOnOutOfMemoryError
-XX:-OmitStackTraceInFastThrow
-ea
-Dsun.io.useCanonCaches=false
-Djdk.http.auth.tunneling.disabledSchemes=""
-Djdk.attach.allowAttachSelf=true
-Djdk.module.illegalAccess.silent=true
-Dkotlinx.coroutines.debug=off

```

## <font color='red'>修改为</font>

```java
server
-Xms2048m
-Xmx2048m
-XX:ReservedCodeCacheSize=500m
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=50
-ea
-Dsun.io.useCanonCaches=false
-Djava.net.preferIPv4Stack=true
-Djdk.http.auth.tunneling.disabledSchemes=""
-XX:+HeapDumpOnOutOfMemoryError

```





#  Debug 首先进入 URlLClassLoader 解决办法

```apl
ctrl + shift + f8进入Breakpoints
```

```ABAP
将Java Exception Breakpoints的checkbox不用勾选
```

