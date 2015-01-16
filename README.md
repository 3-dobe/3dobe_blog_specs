# 3dobe博客写作规范

### 写作规范

#### 标题

* 标题请使用``##``表示一级标题，``###``表示二级标题

#### 代码

* 代码请使用4个空格缩进或者1个tab缩进，不要使用 **```java** 的方式插入代码（HighLight插件的要求）
* 如果贴的代码为开源项目源码需注明文件名，如不注明则默认为上次注明的文件
* 贴代码时不提倡整个函数一次性贴完，当说明文字只需要一个较长函数的一部分代码时，则需要用“空行-......-空行”来表示无用的代码，并同时要展现完整的函数块，如下代码块所示(frameworks/base/services/java/com/android/server/am/ActivityManagerService.java)：
  private ServiceLookupResult retrieveServiceLocked(Intent service,
            String resolvedType, int callingPid, int callingUid) {
        ServiceRecord r = null;
        if (service.getComponent() != null) {
            r = mServices.get(service.getComponent());
        }
        Intent.FilterComparison filter = new Intent.FilterComparison(service);
        r = mServicesByIntent.get(filter);
        if (r == null) {
            
            ......
    
        }
            
        ......
        
    }

#### 空格

* 在书写内容或标题遇到字母、数字、汉字一起出现的情况时，需要在字母与汉字之间、字母与数字之间、汉字与数字之间插入一个空格

### 参考

[MarkDown语法参考](http://wowubuntu.com/markdown/)
