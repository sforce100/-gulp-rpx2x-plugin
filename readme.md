# gulp-rpx2x-plugin #

### 借鉴的是nilhave的gulp-px2rem-plugin

将 rpx 转化成 rem或者其他单位 的 gulp 插件。

### 使用方法 ###
    var gulp = require('gulp');
    var rpx2x = require('gulp-rpx2x-plugin');
    
    gulp.task('default', function() {
      gulp.src('*.css')
      .pipe(rpx2x())
    //  .pipe(rpx2x({'unit_type':px, 'ignore_px':[1,2],'ignore_selector':['.class1']}));
    });

### 参数说明 ###
- ignore_px：让部分px不在转换成rem。默认为空数组
- ignore_selector：让部分选择器不在转换为rem。默认为空数组
- unit_type: 转化单位类型自定义
- base_value: 数值基础，转化乘以这个数字。默认0.0125

### 附加要求 ###
使用 rem 来布局，需要你使用 js 来动态设置 html 的 font-size 值。根据你的参数 pieces 设置，font-size = device-width / pieces。来就是说，如果手机物理像素为320，那么 font-size:32px。
