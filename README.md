
# 背屏日历焦点版 (Calendar Focus)


这是一个专为小米 17 Pro 系列（背屏机型）打造的 MAML 动态小部件。它通过解析系统底层的“焦点通知”数据流，将你的日历日程实时、优雅地呈现在背屏上。
<img width="1123" height="2414" alt="long" src="https://github.com/user-attachments/assets/13374f14-9a10-40f5-9a36-b44def7606c1" />
<img width="1123" height="2414" alt="short" src="https://github.com/user-attachments/assets/2710479c-074b-415b-b1c3-8d3d85f34e7a" />

---

## ✨ 核心特性
### 📅 1. 系统级日程同步 (System Focus Sync)
不同于传统的静态插件，本项目深度集成系统通知监听逻辑：

实时解析：直接抓取 com.android.calendar 的原始数据流。

长文本适配：支持日程标题自动换行（最多2行），并利用动态高度算法自动避让下方时间。

### 📱 2. 灵动外屏适配 (Sub-screen Adaption)

智能嗅探：代码内置 q200 / p2 画幅识别逻辑，根据真实宽高比计算全局缩放系数 #scale。

精准排版：所有 UI 坐标均经过缩放换算，完美对齐左侧摄像头安全区，视觉重心极度稳定。

### 🔋 3. 丝滑 AOD 切换 (Breathable AOD)
复刻官方级动效，兼顾美感与 OLED 屏幕保护：

呼吸渐变：利用小米 Folme 动画引擎，在息屏时实现背景与文字的平滑交叉淡入淡出。

色彩重构：进入 AOD 后，标题自动转为高对比度白色，时间切换为透亮浅蓝（#90CAF9），确保黑底环境下清晰可见。

零帧挂起：严谨遵循 AOD 省电规范，在动画完成回调（onComplete）后彻底挂起引擎（rate="0"），实现极低待机功耗。

