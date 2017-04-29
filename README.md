# SensitiveWordFilter
参考博客[链接](http://cmsblogs.com/?p=1031)
## 匹配模式
> MinMatchType 最小匹配模式<br>MaxMatchType 最大匹配模式

栗子: 假设敏感词库有日本和日本人, 去替换"我不是日本人"的话, 
最小匹配结果是"我不是**人", 而最大匹配结果是"我不是\***"


## 构造方法
### 无参构造方法
根据默认的敏感词库文件生成敏感词库
### 一参构造函数
传入文件的相对路径, 根据指定的敏感词库文本生成敏感词库

## 主要方法
### isContainSensitiveWord
> public boolean isContainSensitiveWord(String txt, int matchType)

判断传入的文本是否为敏感词汇

### replaceSensitiveWords
> public String replaceSensitiveWords(String txt, int matchType) <br>
> public String replaceSensitiveWords(String txt, char replaceChars, int matchType)

传入文本后替换敏感词汇, 如果不指定replaceChars, 则默认使用"*"替换

## 使用
下载io.ride.Sensitive.jar, 添加到工程中即可