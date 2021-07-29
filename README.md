# UnitTestDemo

《iOS单元测试实战》课程Demo项目。课程中出现的所有单元测试用例均能在此项目中找到。

## 目录

[TOC]

## 依赖框架

- XCTest（Xcode自带）
- OCMock

## 注意事项

- 单元测试代码同样需要遵循代码规范
- 为了演示效果，Demo项目中会有一部分运行失败的单元测试，修复方法可以参考课程内容或自行探索。
- 项目中直接将OCMock放在根目录，实际使用时应该根据项目规范引入，比如使用`Pod`引入。

## 目录结构

```shell
/path/to/UnitTestDemo
├── OCMock                  # OCMock框架
├── test.xcresult           # `xcodebuild test`脚本生成的xcresult文件
├── Demo                    # 工程主目录
|   ├── CDataUtil.h/m       # 提供数字转字符串方法的工具类（演示基础单元测试）
|   └── Example            
|       ├── CDemoUtil.h/m   # 演示异步代码验证和OCMock方法调用验证
|       ├── CUserItem.h/m   # 演示代码拆分，提升代码可测试性
|       └── CUserView.h/m   # 演示代码解藕，UI和数据分离，提升代码可测试性
└── DemoTests               # 单元测试主目录
    ├── CDataUtilTest.m     # 基础单元测试用例类
    ├── CDataUtilTest2.m    # 使用OCMock的单元测试用例类
    └── Example                
        ├── CDemoUtilTest.m  # 异步单元测试和方法调用验证
        └── CUserItemTest.m  # 方法拆分后单元测试验证
```

## 主要技术栈

- ObjectiveC
- Shell
