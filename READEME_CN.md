# AlphaTabsIndicator
高仿微信底部状态栏的轻量级库，适用多数底部状态栏应用需求
## 摘要
仿微信底部tab标签，滑动的时候颜色渐变，增加角标功能, 使用极其简单，只需要两行代码。

## 英文文档
[View English Documents](https://github.com/yingLanNull/AlphaTabsIndicator)

## 动画
![1](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/show.gif)

## 截图
![1](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/Screenshot1.png)
![2](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/Screenshot2.png)
![3](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/Screenshot3.png)
![4](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/Screenshot4.png)

## 下载APK体验
[点击下载](https://github.com/yingLanNull/AlphaTabsIndicator/blob/master/show/app-debug.apk)

## 使用方法
### 步骤 1
#### Gradle 配置
```
dependencies {
    compile 'com.yinglan.alphatabs:library:1.0.6'
}
```

### 步骤 2

#### 布局使用
```
	        <com.yinglan.alphatabs.AlphaTabsIndicator
                android:id="@+id/alphaIndicator"
                android:layout_width="match_parent"
                android:layout_height="55dp"
                android:orientation="horizontal">

                <com.yinglan.alphatabs.AlphaTabView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:padding="5dp"

                    app:tabIconNormal=""
                    app:tabIconSelected=""
                    app:tabText=""
                    app:tabTextSize=""
                    app:textColorNormal=""
                    app:textColorSelected=""
                    app:badgeBackgroundColor=""
                    app:paddingTexwithIcon=""/>

                <com.yinglan.alphatabs.AlphaTabView
                    android:layout_width="0dp"
                    android:layout_height="match_parent"
                    android:layout_weight="1"
                    android:padding="5dp"

                    app:tabIconNormal=""
                    app:tabIconSelected=""
                    app:tabText=""
                    app:tabTextSize=""
                    app:textColorNormal=""
                    app:textColorSelected=""
                    app:badgeBackgroundColor=""
                    app:paddingTexwithIcon=""/>

                    、、、、
                    、、、、

            </com.yinglan.alphatabs.AlphaTabsIndicator>                                //模式
```
#### 功能与参数定义

<table>
  <tdead>
    <tr>
      <th align="center">配置参数</th>
      <th align="center">参数含义</th>
    </tr>
  </tdead>
  <tbody>
    <tr>
      <td align="center">tabIconNormal</td>
      <td align="center">未选中的图标</td>
    </tr>
    <tr>
      <td align="center">tabIconSelected</td>
      <td align="center">已经选中的图标</td>
    </tr>
    <tr>
      <td align="center">tabText</td>
      <td align="center">tab标签的文字</td>
    </tr>
    <tr>
      <td align="center">tabTextSize</td>
      <td align="center">tab标签的文字大小</td>
    </tr>
    <tr>
      <td align="center">textColorNormal</td>
      <td align="center">未选中的文字颜色</td>
    </tr>
    <tr>
      <td align="center">textColorSelected</td>
      <td align="center">已选中的文字颜色</td>
    </tr>
    <tr>
       <td align="center">badgeBackgroundColor</td>
       <td align="center">角标背景色,默认红色</td>
     </tr>
     <tr>
       <td align="center">paddingTexwithIcon</td>
       <td align="center">图标和文字之间的距离</td>
     </tr>
  </tbody>
</table>


#### 代码

##### AlphaTabView 主要方法
```
        mAlphaTabView.showNumber(int i); //显示数字角标
        mAlphaTabView.showPoint();       //显示小红点
        mAlphaTabView.removeShow();      //移除当前角标
```

##### AlphaTabsIndicator 主要方法
```
        mAlphaTabsIndicator.setViewPager(ViewPager mViewPger);                     //设置ViewPager
        mAlphaTabsIndicator.setOnTabChangedListner(OnTabChangedListner listner);   //设置底部tab点击监听
        mAlphaTabsIndicator.removeAllBadge();                                      //移除所有tab的角标
        mAlphaTabsIndicator.setTabCurrenItem(int tabIndex);                        //设置tab选项
```

#### 说明
本库是在征得[jeasonlzy](https://github.com/jeasonlzy)的许可后,在其[AlphaIndicatorView](https://github.com/jeasonlzy/AlphaIndicatorView)基础上做的易用性改进,感谢,现持续开源。
## 改进项主要有:
1. 增加角标,使其更接近微信底部tab;
1. 对角标的大小进行动态控制,会根据tab高度自适应;
1. 对使用要求限制适当降低,可以在不绑定viewpager的情况下使用;
1. 增加点击tab的监听回调;
1. 图标和文字之间的距离可以配置,默认为5;
1. 增加在不绑定ViewPager时可设置tab选项;
1. 增加在代码mViewPager.setCurrentItem(i)控制状态下tab联动;
1. 修复在未设置状态下不能点击Tab的问题。
