---
parmalink: /werewolf/
layout: default
---

今天我想写一个狼人杀游戏，准备实现以下功能：
  * 记录日志
  * 六人游戏
  * 多语言支持
  * 基本角色分配，2个狼人 ，2个平民 ，1个预言家，1个女巫

角色能力如下：

|角色|能力|
|---|---|
|平民|无|
|狼人|每晚商议击杀一名玩家|
|女巫|可以击杀一名玩家和复活一名被狼人击杀的玩家|
|预言家|每晚可以知道某名玩家是否是狼人|

文件结构如下：

    Werewolf (项目文件夹) ┬ locales ┬ cn.json (中文翻译)
                         |         └ en.json (英文翻译)
                         ├lang.py (加载语言)
                         └main.py (主程序)

对于lang模块，会内置load与t函数，load接受参数lang，默认为'cn'，表示语言，用于读取翻译文件，并存入字典，方便在t中查找。

在main模块中，需要导入logging、lang、os、sys、time库。我们定义了以下模块：

| 函数名 | 功能 |
| --- | --- |
|clear_screen|清屏|
|input_int|输入一个整数并检查合法性|
|show_game_state|输出游戏状态|
|check_win_condition|检查游戏结束|
|werewolf|狼人行动|
|witch|女巫行动|
|prophet|预言家行动|
|press_enter_to_continue|按Enter键继续|

对于这个游戏，还有许多改进点：
  * 远程翻译文件
  * AI玩家
  * 添加插件包机制
  
目前，源代码已经发布并开源在 https://github.com/husanle/Werewolf/ ，希望大家能多多提出建议。






