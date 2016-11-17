# XYMScan
原生扫码简单封装，扫描二维码和条形码。可基于这个扫码View结合自己的业务需求进行深度定制。

##使用
...
#import "XYMScanView.h"
...

遵守协议
...
@interface XYMScanViewController ()<XYMScanViewDelegate>
...

在你要用到的控制器里面创建View（宽高设置为屏幕宽高）
...
XYMScanView *scanV = [[XYMScanView alloc]initWithFrame:CGRectMake(0, 0, ScreenWidth, ScreenHeight)];
scanV.delegate = self;
[self.view addSubview:scanV];
...

设置扫码框的宽度，默认是250（正方形）
...
scanV.scanW = 250;
...

实现代理方法（拿到扫码的数据scanDataString）
...
-(void)getScanDataString:(NSString*)scanDataString{
}
...

提供两个对象方法（开始扫码，结束扫码）
...
- (void)startRunning;
- (void)stopRunning;
...
