## 步骤记录

> [官方项目地址](https://github.com/KittenML/KittenTTS)
> 
> [模型kitten-tts-nano-0.1](https://huggingface.co/KittenML/kitten-tts-nano-0.1)
> 
> 使用平台(macOS m2)



### 1. 实验步骤

```shell
# 安装 espeak-ng 来处理运行 RuntimeError: espeak not installed on your system
brew install espeak-ng

# 同步依赖
uv sync

# 运行前执行(临时)
export PHONEMIZER_ESPEAK_PATH=/opt/homebrew/bin/espeak-ng
export PHONEMIZER_ESPEAK_LIBRARY=/opt/homebrew/lib/libespeak-ng.dylib

uv run demo.py
```

### 2. 结论


- CPU 可运行
- 使用的是 `ONNX`
- 不支持中文
- 声音不够自然
- 结尾会出现吞字现象(建议添加 `?!.` 等符号测试)