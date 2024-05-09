# Kotlin for LaTeX Listings Plus
 [English](https://github.com/JunSilckTar/Kotlin-for-LaTeX-Listings-Plus?tab=readme-ov-file)  

一个支持 [Kotlin](https://kotlinlang.org/)  语言的 Latex模板

在 [**Kotlin for LaTeX Listings**](https://github.com/cansik/kotlin-latex-listing?tab=readme-ov-file)  的基础上修改

主题参考了 Xcode

![image](https://github.com/JunSilckTar/Kotlin-for-LaTeX-Listings-Plus/blob/main/png/main.png)

## 如何使用?

##### 第一步

下载在**TexConfig**文件夹里的 **Kotlin.tex** 和 **package.tex**  

或者直接复制 **Kotlin.tex** 里的代码到你任意的 .tex 文件里 

![image](https://github.com/JunSilckTar/Kotlin-for-LaTeX-Listings-Plus/blob/main/png/config.png)

如果你选择复制代码或者只使用 **Kotlin.tex**, 你需要检查宏依赖

删除 **\input{TexConfig/package}**

添加 **\usepackage[dvipsnames]{xcolor}**  **\usepackage{listings}** 和 **\usepackage{fontspec}**

```latex
% 在Kotlin.tex里删除这一句
\input{TexConfig/package}

% 在Kotlin.tex里添加以下宏依赖
\usepackage[dvipsnames]{xcolor}
\usepackage{listings}
\usepackage{fontspec}
```



##### 第二步

导入 **Kotlin.tex** 文件，可以选择在main.tex里导入，就像这样

```latex
\documentclass[a4paper, 11pt]{report}
\input{TexConfig/Kotlin} %  检查Kotlin.tex文件的位置
\title{My First Document}
```



##### 第三步

使用方式一:

```latex
\begin{lstlisting}[caption={print something}, label={lst:kt}, language=Kotlin]
// this is a simple code of kotlin:
println("hello kotlin from latex")
\end{lstlisting}
```

看起来就像这样:
![截屏2024-05-09 17.46.36](https://github.com/JunSilckTar/Kotlin-for-LaTeX-Listings-Plus/blob/main/png/print.png)





使用方式二:

``````latex
\lstinputlisting[label={lst:kt3}, language=Kotlin]{Kotlin/Test.kt}
``````

![截屏2024-05-09 17.46.36](https://github.com/JunSilckTar/Kotlin-for-LaTeX-Listings-Plus/blob/main/png/text.png)



建议您将代码拆分为不同的文件，或使用第一种方式

## 自定义主题

```Latex
% 使用 \lstdefinelanguage 定义语言
\lstdefinelanguage{languageName}{
    style = styleName,
}
% 使用 \lstdefinestyle 定义语言的主题
\lstdefinestyle{styleName}{
		basicstyle=\normalfont\ttfamily\normalsize,
		more style setting...
}

```

## 感谢

感谢前辈的辛苦工作 [@cansik](https://github.com/cansik)

 
