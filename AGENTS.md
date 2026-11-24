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

## Harness / Loop（助手）

- 遵循根 `/Users/skat/AGENTS.md`：**Harness Engineering** + **Loop Engineering**
- Guide = 本文件；Sensor = 下方验证命令；同类失误第二次须沉淀规则或测试（棘轮）
- 开干前写清 **Done**；每切片过验证环；显式停止（成功 / 上限 / 无进展 / 人审）
- 详解：`docs/HARNESS_ENGINEERING.md`、`docs/LOOP_ENGINEERING.md`

## 验证环 / Done

```bash
npm install
npm test          # 若有
npm run build     # 或 build:web
npx cap sync android   # 若有 android/
# 可选：JAVA_HOME=…/openjdk@17 npm run apk:debug
```

**Done 示例**：测试通过（若有）+ web 产物进 `www/`/`dist/` + `cap sync` 无报错。可选穿戴未做可搁置，不纳入强制 Done。
