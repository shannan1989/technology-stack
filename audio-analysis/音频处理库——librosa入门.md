- [序言](#%e5%ba%8f%e8%a8%80)
- [安装](#%e5%ae%89%e8%a3%85)
  - [pypi](#pypi)
  - [conda](#conda)
- [常用功能](#%e5%b8%b8%e7%94%a8%e5%8a%9f%e8%83%bd)
  - [核心音频处理函数](#%e6%a0%b8%e5%bf%83%e9%9f%b3%e9%a2%91%e5%a4%84%e7%90%86%e5%87%bd%e6%95%b0)
    - [音频处理](#%e9%9f%b3%e9%a2%91%e5%a4%84%e7%90%86)
    - [频谱表示](#%e9%a2%91%e8%b0%b1%e8%a1%a8%e7%a4%ba)
    - [幅度转换](#%e5%b9%85%e5%ba%a6%e8%bd%ac%e6%8d%a2)
    - [时频转换](#%e6%97%b6%e9%a2%91%e8%bd%ac%e6%8d%a2)
  - [特征提取](#%e7%89%b9%e5%be%81%e6%8f%90%e5%8f%96)
  - [绘图显示](#%e7%bb%98%e5%9b%be%e6%98%be%e7%a4%ba)
- [常用功能代码实现](#%e5%b8%b8%e7%94%a8%e5%8a%9f%e8%83%bd%e4%bb%a3%e7%a0%81%e5%ae%9e%e7%8e%b0)
  - [读取音频](#%e8%af%bb%e5%8f%96%e9%9f%b3%e9%a2%91)
  - [特征提取](#%e7%89%b9%e5%be%81%e6%8f%90%e5%8f%96-1)
    - [提取 Log-Mel Spectrogram 特征](#%e6%8f%90%e5%8f%96-log-mel-spectrogram-%e7%89%b9%e5%be%81)
    - [提取 MFCC 特征](#%e6%8f%90%e5%8f%96-mfcc-%e7%89%b9%e5%be%81)
  - [绘图显示](#%e7%bb%98%e5%9b%be%e6%98%be%e7%a4%ba-1)
    - [绘制声音波形](#%e7%bb%98%e5%88%b6%e5%a3%b0%e9%9f%b3%e6%b3%a2%e5%bd%a2)
    - [绘制频谱图](#%e7%bb%98%e5%88%b6%e9%a2%91%e8%b0%b1%e5%9b%be)

# 序言
librosa是一个用于对音频/音乐进行分析/处理的Python工具包，一些常见的时频处理、特征提取、绘制声音图形等功能应有尽有。

# 安装

## pypi
最简单的方法就是用 pip 安装，可以满足所有的依赖关系
```
pip install librosa
```
## conda
如果安装了Anaconda，可以通过conda命令安装：
```
conda install -c conda-forge librosa
```

# 常用功能

## 核心音频处理函数
这部分介绍了最常用的音频处理函数，包括音频读取函数load()，重采样函数resample()，短时傅里叶变换stft()，幅度转换函数amplitude_to_db()以及频率转换函数hz_to_mel()等。

这部分函数很多，详细参见 http://librosa.github.io/librosa/core.html

### 音频处理
![音频处理](./image/librosa/core1.png)

### 频谱表示
![频谱表示](./image/librosa/core2.png)

### 幅度转换
![幅度转换](./image/librosa/core3.png)

### 时频转换
![时频转换](./image/librosa/core4.png)

## 特征提取
列举了一些常用的频谱特征提取方法，包括常见的Mel Spectrogram、MFCC、CQT等。

详细参见 http://librosa.github.io/librosa/feature.html

![特征提取](./image/librosa/feature.png)

## 绘图显示
包含了常用的频谱显示函数specshow(), 波形显示函数waveplot()等

详细参见 http://librosa.github.io/librosa/display.html

![绘图显示](./image/librosa/display.png)

# 常用功能代码实现

## 读取音频

## 特征提取

### 提取 Log-Mel Spectrogram 特征

### 提取 MFCC 特征

## 绘图显示

### 绘制声音波形

### 绘制频谱图
