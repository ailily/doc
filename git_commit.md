Git使用规范
===========
# 提交记录格式：
每次提交，Commit message 都包括三个部分：Header，Body 和 Footer。
```
    <type>(<scope>): <subject>
    <空一行>
    <body>
    <空一行>
    <footer>
```
其中，Header 是必需的，Body 和 Footer 可以省略。
不管是哪一个部分，任何一行都不得超过72个字符（或100个字符）。这是为了避免自动换行影响美观。
## Header
Header部分只有一行，包括三个字段：type（必需）、scope（可选）和subject（必需）。
### type
type用于说明 commit 的类别，使用以下9个标识。
* feat：新功能（feature）
* fix：bug修复
* docs：文档（documentation）
* style： 格式（不影响代码运行的变动）
* refactor：重构（即不是新增功能，也不是修改bug的代码变动）
* test：增加测试
* perf：性能优化
* chore：构建过程或辅助工具的变动
* revert：撤销上一次的commit
### scope
scope用于说明 commit 影响的范围，使用以下3个标识
* all：表示影响面大，如修改了框架，会对整个程序产生影响
* module：表示会影响某个模块，如实时监控模块、报警查询模块、企业与用户管理模块等等
* location：表示影响小，某个小小的功能
### subject
subject是 commit 目的的简短描述，不超过50个字符。
* 使用第一人称现在时，例：“修改xxx”而不要写“修改了xxx”
* 第一个字母小写
* 结尾不加句号
## body
具体的修改信息，应该尽量详细
* 使用第一人称现在时，例：“修改xxx”而不要写“修改了xxx”
* 包括变动的原因和与之前的对比
## footer
备注信息，如果与redmine关联（包括bug，task等），则为：close #{id}，将{id}替换为真实的id
## 示例
```
feat(module): 报表管理-添加用户在线时长报表

新增了UserOnlineTimeController
```
```
fix(module): 报表管理-修复用户在线时长报表分页显示问题

修复解析前台参数的错误

close #8345
```
# 提交合并请求规范
提交的分支内容不能同时包含新功能与bug修复
# 合并请求格式
参考代码提交记录格式
