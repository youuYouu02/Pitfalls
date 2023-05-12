vscode 输出中文乱码

> vscode 默认保存为 utf-8，但 cmd 默认格式为 GBK

通过编码保存 - GBK - 通过编码重新打开 - GBK



为什么会出现乱码？

如果UTF-8编码的文本文件中包含某些特殊的Unicode字符（例如中文），那么在GBK格式下会被错误理解，即乱码。

