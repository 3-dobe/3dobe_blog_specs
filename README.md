# 3dobe 博客写作规范

### 说明

本博客一律使用markdown语法编写。

### 写作规范

#### 1. 标题

1. 标题请使用 ``##`` 表示一级标题，``###`` 表示二级标题，依此类推

#### 2. 代码

1. 代码请使用 4 个空格缩进或者 1 个 tab 缩进，不要使用 **```java** 的方式插入代码（HighLight 插件的要求）
 
2. 如果贴的代码为开源项目源码需注明文件名，如不注明则默认为上次注明的文件
 
3. 贴代码时不提倡整个函数一次性贴完，当说明文字只需要一个较长函数的一部分代码时，则需要用“空行-......-空行”或者“空格-......空格”来表示无用的代码，并同时要展现完整的函数块，如下代码块所示(frameworks/base/services/java/com/android/server/am/ActivityManagerService.java)：

        private ServiceLookupResult retrieveServiceLocked(Intent service,
                String resolvedType, int callingPid, int callingUid) {
            ServiceRecord r = null;
            if (service.getComponent() != null) {
                r = mServices.get(service.getComponent());
            }
            Intent.FilterComparison filter = new Intent.FilterComparison(service);
            r = mServicesByIntent.get(filter);
            if (r == null) { ...... }
            
            ......
        
        }

### 参考

[MarkDown语法参考](http://wowubuntu.com/markdown/)
