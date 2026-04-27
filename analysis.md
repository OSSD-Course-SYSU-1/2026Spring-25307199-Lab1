PlayShortVideosBasedOnVideoComponent-master/ 
│
├── .idea/                                          # IDE配置目录
│   ├── .deveco/                                    # DevEco项目缓存
│   │   ├── cxx/                                    # C++相关缓存
│   │   ├── module/                                 # 模块缓存
│   │   │   ├── entry.cache.json
│   │   │   └── project.cache.json
│   │   └── modules/
│   │       ├── entry.iml
│   │       └── PlayShortVideosBasedOnVideoComponent-master.iml
│   ├── .gitignore
│   ├── modules.xml
│   └── workspace.xml                               # 工作区配置
│
├── .hvigor/                                        # Hvigor构建缓存
│   ├── cache/
│   │   ├── file-cache.json
│   │   ├── meta.json
│   │   └── task-cache.json
│   ├── dependencyMap/                              # 依赖映射
│   │   ├── entry/
│   │   │   ├── oh-package.json5
│   │   │   └── dependencyMap.json5
│   │   └── oh-package.json5
│   ├── outputs/                                    # 构建输出
│   │   ├── build-logs/
│   │   ├── logs/
│   │   └── sync/
│   └── report/
│       └── report-202604211651042990.json
│
├── AppScope/                                       # 应用全局配置
│   ├── app.json5                                   # 应用配置(包名/版本/图标)
│   └── resources/
│       └── base/
│           ├── element/
│           │   └── string.json                     # 字符串资源
│           └── media/
│               ├── background.png                  # 图标背景层
│               ├── foreground.png                  # 图标前景层
│               └── layered_image.json              # 分层图标配置
│
├── entry/                                          # 主模块
│   │
│   ├── build/                                      # 编译构建产物
│   │   ├── cache/                                  # 编译缓存
│   │   ├── config/
│   │   │   └── buildConfig.json
│   │   ├── default/                                # 默认构建配置
│   │   │   ├── cache/
│   │   │   ├── generated/
│   │   │   ├── intermediates/
│   │   │   └── outputs/                            # HAP/APP输出
│   │   └── ...
│   │
│   ├── src/                                        # 源码目录
│   │   └── main/
│   │       │
│   │       ├── ets/                                # ArkTS源码
│   │       │   │
│   │       │   ├── common/                         # 公共工具类
│   │       │   │   ├── TimeUtil.ets                # 时间格式化工具
│   │       │   │   ├── LogUtil.ets                 # 日志工具
│   │       │   │   └── ScreenUtil.ets              # 屏幕适配工具
│   │       │   │
│   │       │   ├── constants/                      # 常量定义
│   │       │   │   ├── VideoConstants.ets          # 视频相关常量
│   │       │   │   ├── GestureConstants.ets        # 手势阈值常量
│   │       │   │   └── AppConstants.ets            # 应用通用常量
│   │       │   │
│   │       │   ├── entryability/                   # 应用入口
│   │       │   │   └── EntryAbility.ets            # 生命周期管理
│   │       │   │       ├── onCreate()              # 创建时初始化
│   │       │   │       ├── onBackground()          # 后台处理
│   │       │   │       ├── onForeground()          # 前台处理
│   │       │   │       └── onDestroy()             # 销毁时释放资源
│   │       │   │
│   │       │   ├── entrybackupability/             # 数据备份
│   │       │   │   └── EntryBackupAbility.ets
│   │       │   │
│   │       │   ├── pages/                          # 页面目录
│   │       │   │   └── Index.ets                   # 视频播放主页面
│   │       │   │       ├── Video组件               # 视频播放核心
│   │       │   │       ├── 手势处理                # 点击/长按/滑动
│   │       │   │       ├── 播放控制                # 播放/暂停/倍速
│   │       │   │       └── 全屏切换                # 横竖屏切换
│   │       │   │
│   │       │   └── view/                           # 自定义组件
│   │       │       ├── VideoProgressBar.ets        # 进度条组件
│   │       │       │   ├── Slider控件              # 进度拖动
│   │       │       │   ├── 时间显示                # 当前/总时长
│   │       │       │   └── seek()跳转              # 跳转指定位置
│   │       │       │
│   │       │       ├── VolumeControlBar.ets        # 音量控制条
│   │       │       │   ├── 垂直滑动条              # 音量调节
│   │       │       │   ├── 音量图标                # 静音/有声状态
│   │       │       │   └── setVolume()             # 设置系统音量
│   │       │       │
│   │       │       └── SpeedIndicator.ets          # 倍速提示
│   │       │           ├── 1.0x显示                # 正常速度
│   │       │           └── 2.0x显示                # 倍速状态
│   │       │
│   │       └── resources/                          # 资源目录
│   │           │
│   │           ├── base/                           # 基础资源
│   │           │   ├── element/
│   │           │   │   ├── color.json              # 颜色定义
│   │           │   │   └── string.json             # 字符串
│   │           │   └── media/
│   │           │       └── icon.png
│   │           │
│   │           ├── dark/                           # 深色模式资源
│   │           │   ├── element/
│   │           │   │   └── color.json              # 深色颜色
│   │           │   └── media/
│   │           │
│   │           ├── en_US/                          # 英文资源
│   │           │   └── element/
│   │           │       └── string.json
│   │           │
│   │           ├── zh_CN/                          # 中文资源
│   │           │   └── element/
│   │           │       └── string.json
│   │           │
│   │           └── rawfile/                        # 原始文件
│   │               ├── video_01.mp4                # 短视频文件1
│   │               ├── video_02.mp4                # 短视频文件2
│   │               └── video_03.mp4                # 短视频文件3
│   │
│   ├── .gitignore                                  # Git忽略配置
│   ├── build-profile.json5                         # 模块构建配置
│   ├── hvigorfile.ts                               # 模块构建脚本
│   ├── module.json5                                # 模块配置(Ability/权限)
│   ├── obfuscation-rules.txt                       # 混淆规则
│   └── oh-package.json5                            # 模块依赖配置
│
├── hvigor/                                         # Hvigor构建配置
│   └── hvigor-config.json5
│
├── screenshots/                                    # 效果截图
│   ├── effect_01.png                               # 播放界面
│   ├── effect_02.png                               # 进度条拖动
│   ├── effect_03.png                               # 音量调节
│   └── effect_04.png                               # 全屏模式
│
├── build-profile.json5                             # 工程构建配置
├── code-linter.json5                               # 代码检查规则
├── hvigorfile.ts                                   # 工程构建脚本
├── LICENSE                                         # 开源协议
├── OAT.xml                                         # 开源审计配置
├── oh-package.json5                                # 工程依赖配置
└── README.md                                       # 项目说明