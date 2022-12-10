# day22 GUI

## 交互方式

- GUI(Graphic User Interface  图形化用户接口)
- CLI(Command Line User Interface 命令行用户接口)

## Awt 和Swing

- java.Awt:Abstract windows toolkit (抽象窗口工具包),需要调用本地系统方法实现功能,属于重量级控件
- javax.Swing: 在Awt基础上,建立的一套图形界面系统,其中提供了更多的组件,而且,完全由java实现.增强了移植性,属于轻量级控件.

## 图形组件包中的工具
- Component

  - botton
  - label
  - checkbox
  - textComponent
    - TextArea
    - TextField
- Container

  - window
    - frame
    - dialog
      - FileDialog
  - panel

## 布局管理器

- 容器中组件的排放方式就是布局
- FlowLayout(流式布局管理器)
  - 从左到右的数序排列
  - pannel默认的布局管理器

- BorderLayout(边界布局管理器)
  - 东南西北中
  - Frame默认的布局管理器

- GridLayout(网络布局管理器)
  - 规则的矩阵

- CardLayout(卡片布局管理器)
  - 选项卡

- GridBagLayout(网络包布局管理器)
  - 非规则的矩阵(多个网格合并)

- 坐标式布局管理器





  