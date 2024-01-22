# 

## roadmap

 - [ChinesePinyinIntelliSenseExtender](https://github.com/stratosblue/ChinesePinyinIntelliSenseExtender)
    - 修改插件名称及包名称，由于现在理论上可以支持任意表意文字，不局限于中文，考虑新开项目还是修改；
    - 在智能感知时判断输入环境，当不处于联想上下文时，提供候选字，该功能类似于在`VisualStudio`内实现一个简单的输入法，以在不切换系统输入法的情况下，快速输入其他语言文字；

 - [IntelliSenseLocalizer](https://github.com/stratosblue/IntelliSenseLocalizer)
    - 提供`repack`命令，该命令可以使用 `None` 对照类型的包直接重新打包其他对照类型的包，此举可以减少需要上传的语言包数量，并提升用户自由度；
    - 抽象并独立`翻译`流程，现有的基于[在线文档](https://docs.microsoft.com/)的本地化作为默认`翻译`方式，以使用户有更多选择，功能点包括但不限于：
        - 多种翻译引擎的接入；
        - 友好的翻译结果缓存机制；
    - 基于抽象并独立的`翻译`流程支持`第三方库`的本地化；
    - 本地化包的在线分享；

 - [KeenConveyance](https://github.com/stratosblue/KeenConveyance)
    - 使用基于 `0123456789abcdefghijklmnopqrstuvwxyz` 的纯小写字符编码来替代当前的 `URIEncode` 进行方法签名展示，使其更传输友好；

 - [Juxtapose](https://github.com/stratosblue/Juxtapose)
    - 便捷的基于内存共享的结构体数据传输，以减少在参数对象数量较多时序列化反序列化的性能消耗占比；
    - 进一步优化外部进程激活器工作逻辑，使其不限于本地进程；

 - [FluentWorkflow](https://github.com/stratosblue/FluentWorkflow)
    - 内置对数据库事务的接入；
    - 提供数据面板，提供查看流程信息、流程重试、流程终止等操作；

 - [Cuture.AspNetCore.ResponseAutoWrapper](https://github.com/stratosblue/Cuture.AspNetCore.ResponseAutoWrapper)
    - 使用 [SourceGenerator](https://learn.microsoft.com/zh-cn/dotnet/csharp/roslyn-sdk/source-generators-overview) 减少运行时动态类型生成；
    - `MinimalAPI`的支持？

 - [LightweightObjectMapper](https://github.com/stratosblue/LightweightObjectMapper)
    - 使用 [Interceptor](https://learn.microsoft.com/zh-cn/dotnet/csharp/whats-new/csharp-12#interceptors) 以支持更复杂的环境，及更好的性能；

 - [Cuture.Http](https://github.com/cuture/Cuture.Http)
    - 基于 [LLHTTP](https://github.com/dotnet/runtimelab/tree/feature/LLHTTP2) 重写底层请求，以进一步提升性能；

 - [Cuture.Extensions.Modularity](https://github.com/cuture/Cuture.Extensions.Modularity)
    - 使用 [SourceGenerator](https://learn.microsoft.com/zh-cn/dotnet/csharp/roslyn-sdk/source-generators-overview) 减少运行时动态方法调用和反射，包括但不限于：
        - 为自动注入的类型实现基于Factory的DI注入代码；
        - 为Options实现手动绑定代码；
        - 为模块依赖提供依赖模块发现方法，而非现在的反射查找；

-------

## feasible

 - [NativeMemoryStore](https://github.com/stratosblue/ChinesePinyinIntelliSenseExtender/tree/main/src/Ref/NativeMemoryStore)
    - 考虑将 [ChinesePinyinIntelliSenseExtender](https://github.com/stratosblue/ChinesePinyinIntelliSenseExtender) 中使用的 `NativeMemoryStore` 独立为单独的项目，并提供Nuget包；
    - 优化现有实现；
    - 实现压缩和保存、载入功能；

 - [StringTrie](https://github.com/stratosblue/ChinesePinyinIntelliSenseExtender/tree/main/src/Ref/StringTrie)
    - 考虑将 [ChinesePinyinIntelliSenseExtender](https://github.com/stratosblue/ChinesePinyinIntelliSenseExtender) 中使用的 `StringTrie` 独立为单独的项目，并提供Nuget包；

 - [InputMethodDictionary](https://github.com/stratosblue/ChinesePinyinIntelliSenseExtender/tree/main/src/Ref/InputMethodDictionary)
    - 考虑将 [ChinesePinyinIntelliSenseExtender](https://github.com/stratosblue/ChinesePinyinIntelliSenseExtender) 中使用的 `InputMethodDictionary` 独立为单独的项目，并提供Nuget包；

-------

## rhapsody

 - 实现一个`VisualStudio`插件，可以方便的进行代码片段管理，功能包括但不限于：
    - 在线分享代码片段
    - 在线安装、卸载/管理已安装代码片段
    - 基于用户的代码片段漫游

 - 实现一套机制，使`C#`支持任意自定义`语法`/`语法糖`，其在编译前展开为标准`语法`/`语法糖`，理想工作原理类似`using`、`await`/`async`，类比 `TypeScript` -> `JavaScript`；

-------
