## 自定义Protobuf插件
基于Protobuf的扩展语法，通过插件自动生成rpc和rest相关代码

### 定义protobuf

### 自定义插件
可以通过实现 github.com/golang/protobuf/protoc-gen-go/generator 中的Plugin
- Name：插件名
- Init：初始化
- Generate：生成代码
- GenerateImports：生成导入包

#### 生成代码
1. 自定义生成实体「ServiceInfo」
2. 根据生成实体自定义解析器「buildServiceInfo」
3. 根据解析器自定义生成模板 『genCode』

