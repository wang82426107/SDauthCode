# SDauthCode
一个基于Core Graphics框架的本地动态验证码

![](http://upload-images.jianshu.io/upload_images/1396375-8f08828b1495f341.gif?imageMogr2/auto-orient/strip)

</br>
</br>
#### 一行代码快速生成验证码
***



首先,我们把```SDauthCode.h```和```SDauthCode.m```两个文件导入所需要的工程当中去.




使用SDauthCode快速生成验证码,我们只需要一个初始化方法即可.无需繁琐步骤,即可快速生成.代码如下.




```
    SDauthCode *codeView = [[SDauthCode alloc]initWithFrame:CGRectMake(100, 100, 200, 40)];

```



只要把上面的codeView添加到所需要放置的位置上即可.

```
    [self.view addSubview:codeView];

```


那么如何验证用户是否输入正确呢?SDauthCode有个属性叫做authCodeString,我们只需要把输入的字符串和authCodeString比较即可.
```
    if ([codeView.authCodeString isEqualToString:self.textField.text]) {
        
        //这里面写验证正确之后的动作.

        tipWithMessage(@"输入验证码正确");
    }else{
        
        //这里面写验证失败之后的动作.

        tipWithMessage(@"输入验证码错误");
    }
```

