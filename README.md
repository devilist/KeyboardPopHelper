# KeyboardPopHelper
这是一个可以防止键盘弹出时遮挡输入控件的工具类。
当页面有多个edittext时，会自动根据当前获得焦点的edittext进行页面自适应，使输入区域不被键盘遮挡，提高交互体验。

#使用方法

``
KeyboardPopHelper.instance(this)
                .bindEditText(edittext1,edittext2,...)              // 绑定目标edittext
                .bindRootView(findViewById(R.id.scrollview))        // 绑定页面根布局
                .setMonitorFocusSizeChanged(true)                   // 是否监控focusView高度的变化
                .setBottomMargin(10)                                // focusView的bottom
                .setOffset(-100)                                    // 固定模式下的偏移
                .monitor();
``
