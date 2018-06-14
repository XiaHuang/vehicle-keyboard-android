# 停车王车牌号码专用键盘按键切换逻辑说明

> Copyright (c) 2018 Xi'An iRain IoT Technology Service Co.,Ltd

## 一、车牌号码长度

- `新能源车牌`和`武警车牌号码`，其长度为`8`位；
- 其它均为`7`位；

## 二、车牌输入框各序号的键盘布局逻辑

### 2.1 输入框第1位

#### 2.1.1 未知车牌类型

- 默认显示**”民用省份键盘“**，包括”**更多**“按钮；
- 点击“更多”按钮，显示**“首位特殊字符键盘”**；
- 点击”返回“按钮，显示**”民用省份键盘“**；

#### 2.1.2 已知车牌类型

- 以下车牌类型，显示**”首位特殊字符键盘“**，并**禁用”返回“**按钮：
  - 新旧使馆车牌类型；
  - 民航车牌类型；
  - 军队车牌类型；
  - 武警车牌类型；
- 其它类型，显示**”民用省份键盘“**，并**禁用”更多“按钮**；



### 2.2 输入框第2位

| 车牌类型             | 显示键盘布局         | 键位说明                                                |
| -------------------- | -------------------- | ------------------------------------------------------- |
| 民航车牌类型         | **末位特殊字符键盘** | 仅”**航**“字可用，**禁用”返回“**按钮                    |
| 武警车牌类型         | **含I字母+数字键盘** | 仅”**J**“字可用，无”**更多**“、”**返回**“按钮           |
| 军队车牌类型         | **含I字母+数字键盘** | 禁用全部数字，无”**更多**“、”**返回**“按钮              |
| 2017新式使馆车牌类型 | **含I字母+数字键盘** | 禁用全部字母，无”**更多**“、”**返回**“按钮              |
| 旧式大使馆车牌类型   | **含I字母+数字键盘** | 仅`123`数字可用，无”**更多**“、”**返回**“按钮           |
| 其它类型             | **含I字母+数字键盘** | 数字部分，仅`123`数字可用，无”**更多**“、”**返回**“按钮 |

### 2.3 输入框第3-6位

在”武警车牌类型“时，第3位显示**”民用省份键盘“**，并**禁用”更多“按钮**；

其它情况下，显示**”无IO字母+数字键盘“**，**禁用”更多“**按钮；

### 2.4 输入框第7位

| 车牌类型       | 显示键盘布局          | 键位说明             |
| -------------- | --------------------- | -------------------- |
| 港澳车牌类型   | **末位特殊字符键盘**  | 禁用**”返回“**按钮   |
| 使馆车牌类型   | **末位特殊字符键盘**  | 禁用**”返回“**按钮   |
| 领事馆车牌类型 | **末位特殊字符键盘**  | 禁用**”返回“**按钮； |
| 军队车牌类型   | **无IO字母+数字键盘** | 禁用**”更多“**按钮； |
| 其它类型       | **无IO字母+数字键盘** | 开启**”更多“**按钮； |



### 2.5 输入框第8位

新能源车牌类型，显示**”无IO字母+数字键盘“**，**禁用”更多“**按钮；

武警车牌类型，显示**”末位特殊字符键盘“**，禁用**”返回“**按钮；



