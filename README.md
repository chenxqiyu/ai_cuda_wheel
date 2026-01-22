
# 🚀 RTX 50 系列显卡 AI 加速环境

> 适用于 Windows 平台 + ComfyUI + Nunchaku + KJNodes  
> 支持 CUDA 13.0、PyTorch 2.9.1、xFormers、SageAttention、Triton 及 Nunchaku INT4 推理引擎
```
pip install --pre torch==2.9.1+cu130 torchvision==0.24.1+cu130 torchaudio==2.9.1+cu130 --index-url https://download.pytorch.org/whl/cu130
```
```
pip install xformers-0.0.33+5d4b92a.d20260121-cp39-abi3-win_amd64.whl
```
```
pip install triton_windows-3.6.0-cp311-cp311-win_amd64.whl
```
```
pip install sageattention-2.2.0-cp311-cp311-win_amd64.whl
```
```
pip install sageattn3-1.0.0-cp311-cp311-win_amd64.whl
```
```
pip install nunchaku-1.2.0+torch2.9-cp311-cp311-win_amd64.whl
```
```
https://github.com/nunchaku-ai/ComfyUI-nunchaku
https://github.com/kijai/ComfyUI-KJNodes
https://github.com/wallen0322/ComfyUI-SageAttention3
```

```
编译记录

x64 Native Tools Command Prompt for VS 2022

git修复和长路径支持
git config --system core.longpaths true
https://github.com/woct0rdho/triton-windows
https://github.com/mengqin/SageAttention
https://github.com/LagPixelLOL/xformers/tree/blackwell
https://github.com/nunchaku-ai/nunchaku
```