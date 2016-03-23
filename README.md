# Compilers
本文件夹内容为编译原理课程实验的完整内容。课程实验要求从零开始设计一个简单的编译器，能够处理C语言的一些基本语法，并最终生成汇编代码。编译器由三部分构成：词法分析器，语法分析器（采用LR(1)分析法），语义子程序和汇编代码生成。具体内容参见“编译器详解.pdf”

==============
###词法分析器
词法分析器为Main文件夹下的lexical.cpp文件，主要用于识别C语言关键词和c语言变量以及一些其他符号。这部分代码是用c++实现的。

==============
###语法分析器
语法分析器的任务主要是对输入的文法产生式（产生式在gram.txt文本文件中。gram.txt文件中的数字表示终结符，这些终结符应该对应词法分析器中每个token的id号）进行处理，产生Action表（Action.txt）和Goto表（Goto.txt）。语法分析器由python语言实现，程序文件为Yacc.py

==============
###语义子程序和汇编代码生成
程序文件为Main文件夹下的gram.cpp文件，程序功能为更加不同的文法产生式执行不同的操作，将c语言编译成汇编语言。这部分代码用c++实现。

==============
###主程序
主程序为Main文件夹下的main.cpp文件。运行main之前需要先运行Yacc.py，处理gram.txt文本文件里的文法产生式，将Yacc.py生成的Action.txt，Goto.txt以及newg.txt拷贝到Main目录下。运行主程序，编译器的输入为test.c文件（C语言文件），编译器会输出一个文件temp.txt，该文件为编译生成的汇编代码。
