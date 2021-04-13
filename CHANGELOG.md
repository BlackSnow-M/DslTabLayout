# 2020-03-28

版本: '1.5.0', 更新日志:

- `onSelectIndexChange` `onSelectViewChange` `onSelectItemView` 支持 `fromUser`
- `badge` 支持单独为`圆形状态`设置`offset_x` `offset_y`属性
- `badge` 定位`Gravity`支持定位锚点属性`tab_badge_anchor_child_index`
- `badge` 定位支持忽略锚点`padding`属性`tab_badge_ignore_child_padding`
- 调整`DslGravity`定位计算默认输出目标的中心坐标. 可以通过属性`gravityRelativeCenter`关闭.


# 2020-3-12

版本: `1.4.4`, 更新日志:

- `DslTabLayoutConfig`支持文本大小渐变属性配置.

可以通过:
```
tabLayout.configTabLayoutConfig {
    tabTextMinSize = 9 * dp
    tabTextMaxSize = 18 * dp
}
```

# 2020-02-29

版本: `1.4.3-support` ,更新日志:

- 去除`AndroidX`依赖, 兼容`support`版本.

```groovy
    implementation 'com.github.angcyo.DslTabLayout:TabLayout:1.4.3-support'
```

# 2020-02-27

版本: `1.4.3` ,更新日志:

- 修复`child` `CENTER_VERTICAL` 垂直居中`Bottom`坐标计算问题

# 2020-02-22

版本: `1.4.2` ,更新日志:

新增库`Delegate`库:

```groovy
    implementation 'com.github.angcyo.DslTabLayout:ViewPager1Delegate:1.4.2'
    implementation 'com.github.angcyo.DslTabLayout:ViewPager2Delegate:1.4.2'
```

原库的使用方式变成了:

```groovy
    //implementation 'com.github.angcyo:DslTabLayout:1.4.2' 之前
    implementation 'com.github.angcyo.DslTabLayout:TabLayout:1.4.2'
```


# 2020-01-06

版本: `1.4.1` ,更新日志:

+ 新增指示器动画控制属性`tab_indicator_anim`

# 2019-12-16

版本: `1.4.0` ,更新日志:

1. 更友好的`Badge` 角标更新方法
2. 开发全属性角标更新

[WIKI详细说明](https://github.com/angcyo/DslTabLayout/wiki/%E8%A7%92%E6%A0%87)

版本: `1.3.1` ,更新日志:

1. 修复 `Badge` 角标在顶层绘制
2. 新增`Badge` 角标xml属性`tab_badge_text_size`, 角标字体大小配置

# 2019-12-14

版本: `1.3.0` ,更新日志:

1. 支持`ViewPager2`
> 库不依赖`ViewPager`和`ViewPager2`,通过`ViewPagerDelegate`转发事件. 

[请查看WIKI使用说明](https://github.com/angcyo/DslTabLayout/wiki/ViewPager1%E5%92%8CViewPager2)

# 2019-12-13 

版本: `1.2.0` ,更新日志:

1. 修复`child`设置`GONE`之后, `item`平分计算的不正确的问题
2. 修复开启`高凸模式`后, 指示器高度没有过渡的问题
3. 允许指定`文本渐变控件`, 和`图标渐变控件`
4. 修复`tab`切换的时候, 不再强制控制`ViewPager.setCurrentItem`
5. 新增`角标`功能
