//方式一.纯代码设置指定圆角 
https://www.jianshu.com/p/985f6d9f6543

_functionView = [[UIView alloc] initWithFrame:CGRectMake(0, SHeight, SWidth,  FunctionViewHeight )];
_functionView.backgroundColor = [UIColor whiteColor];

       UIBezierPath *maskPath = [UIBezierPath bezierPathWithRoundedRect:_functionView.bounds byRoundingCorners:UIRectCornerTopLeft | UIRectCornerTopRight cornerRadii:CGSizeMake(12, 12)];
       CAShapeLayer *maskLayer = [[CAShapeLayer alloc] init];
       maskLayer.frame = _functionView.bounds;
       maskLayer.path = maskPath.CGPath;
       _functionView.layer.mask = maskLayer;
       
       [self addSubview:_functionView];
       
    
//方式二.使用Xib， 要设置圆角的 view 继承 JQRadiusView ，然后在 IBInspectable 这个窗口可以直接设置圆角
    
