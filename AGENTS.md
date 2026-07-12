# 你哼我猜 (Hum & Guess)

哼唱旋律猜歌名游戏。Web Audio API 实时音高检测 + 旋律匹配。

## 目标平台

| 平台 | 方式 | 产出 |
|------|------|------|
| 🍎 iOS | Capacitor → Xcode | IPA |
| 🤖 Android | Capacitor → Gradle | APK |
| ⌚ 手表 | 触屏自适应 | 同 APK |
| 👓 智能眼镜 | 语音+窄FOV | 同 APK |
| 💍 智能戒指 | DeviceOrientation 倾角 | 上下倾斜→开始/停止录音 |
| 🦯 智能手杖 | DeviceMotion 加速度 | 敲击→切换录音 |

## 技术栈

- Web Audio API 麦克风采集 + 自相关音高检测
- DTW 旋律匹配
- Capacitor 原生包装
