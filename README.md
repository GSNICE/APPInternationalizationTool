# APPInternationalizationTool

App的国际化处理脚本，可以将翻译文档一键转换成 Android 以及 iOS 的格式

### GUI界面

![GUI界面](Image/program_interface.png)

### iOS格式

![iOS格式输出](Image/output_iOS.png)
![iOS格式输出详情](Image/output_iOS_details.png)

### Android格式

![Android格式输出](Image/output_Android.png)
![Android格式输出详情](Image/output_Android_details.png)

## Tips

文本第一行为翻译语言的类型，脚本会根据类型自动生成翻译文本（跟第一列组成key-value形式的翻译文本）
![文本第一行](Image/first_row.png)

文本第一列为翻译文本的索引值，即各国翻译中的key（各国翻译中均有该key，所以这一列不能为空），其他列为各国翻译文本的value值(切换语言的时候会自动换成该文本)
![文本第一列](Image/first_col.png)

**translate.py**
脚本支持txt文本以及Excel表格，但需要引入xlrd，openpyxl这两个库，分别用于xls以及xlsx格式表格的处理

**translate_nolib.py**
脚本不需要引入第三方库，但只支持txt文本，可以将Excel表格中的数据另存为txt文档，或者复制到文本编辑器中生成txt文档(不要使用Windows自带的记事本)，然后使用该脚本一键生成翻译文档

**以上脚本适用于Python 2环境，暂未兼容Python 3（主要原因是Tkinter库的差异，可以修改Tkinter引用，或者直接去掉GUI界面，代码基本能跑通）**



