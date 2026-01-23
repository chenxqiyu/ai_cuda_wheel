<p align="center">
Welcome, the
<a href="https://github.com/chenxqiyu" target="_blank"><img src="https://count.getloli.com/get/@ai_cuda_wheel?theme=rule34" alt="Visitor Counter"></a>
th vistor!
</p>

# 🚀 RTX 50 系列显卡 AI 加速环境（Windows）

> **适用场景**：ComfyUI + Nunchaku + KJNodes  
> **目标**：在 RTX 50 系列显卡上，构建稳定、高性能的 AI 推理与加速环境 ，其他显卡需自行测试

---

## ✨ 环境特性

- ✅ **CUDA 13.0**
- ✅ **PyTorch 2.9.1（cu130）**
- ✅ **xFormers（Blackwell 分支）**
- ✅ **SageAttention2 / SageAttention3**
- ✅ **Triton（Windows 版）**
- ✅ **Nunchaku INT4 推理引擎**
- ✅ **ComfyUI 工作流友好**

---

## 🧩 基础环境

- **操作系统**：Windows 10 / 11 x64  
- **Python**：3.11（推荐）
- **Python version**: 3.11.9 (tags/v3.11.9:de54cf5, Apr  2 2024, 10:12:12) [MSC v.1938 64 bit (AMD64)] 
- **Visual Studio**：VS 2022（含 C++ Build Tools）  
- **显卡**：RTX 50 系列  

---

## 📦 PyTorch（CUDA 13.0）

```bash
pip install --pre torch==2.9.1+cu130 torchvision==0.24.1+cu130 torchaudio==2.9.1+cu130   --index-url https://download.pytorch.org/whl/cu130
```

---

## ⚡ 加速组件安装

### xFormers
```bash
pip install xformers-0.0.33+5d4b92a.d20260121-cp39-abi3-win_amd64.whl
```

### Triton（Windows）
```bash
pip install triton_windows-3.6.0-cp311-cp311-win_amd64.whl
```

### SageAttention
```bash
pip install sageattention-2.2.0-cp311-cp311-win_amd64.whl
```

### SageAttention3
```bash
pip install sageattn3-1.0.0-cp311-cp311-win_amd64.whl
```

### Nunchaku
```bash
pip install nunchaku-1.2.0+torch2.9-cp311-cp311-win_amd64.whl
```

---

## 🧠 ComfyUI 扩展节点

- **Nunchaku**
  - https://github.com/nunchaku-ai/ComfyUI-nunchaku

- **KJNodes**
  - https://github.com/kijai/ComfyUI-KJNodes

- **SageAttention3**
  - https://github.com/wallen0322/ComfyUI-SageAttention3

---

## 🛠️ 编译与构建记录

### 编译环境
- **工具**：x64 Native Tools Command Prompt for VS 2022

### Git 长路径支持（必做）
```bash
git config --system core.longpaths true
```

### 相关源码仓库

- Triton Windows 适配  
  https://github.com/woct0rdho/triton-windows

- SageAttention  
  https://github.com/mengqin/SageAttention

- xFormers（Blackwell）  
  https://github.com/LagPixelLOL/xformers/tree/blackwell

- Nunchaku Core  
  https://github.com/nunchaku-ai/nunchaku

---

## 🧪 实践建议

- 🔹 优先验证 `torch.cuda.is_available()` 与 CUDA 版本一致性  
- 🔹 遇到 `misaligned address`，优先检查 attention kernel / dtype / head_dim  
- 🔹 SageAttention3 与 xFormers 不建议同时启用同一路径  
- 🔹 INT4 推理建议搭配 **Nunchaku + FP16 输入**

---

## 📌 备注

本环境主要面向 **RTX 50（Blackwell）** 架构实验与高性能推理，  
部分组件为 **非官方 / 实验性构建**，请自行评估稳定性。

---
## 使用sageattention3加速选其中一个就行
<img width="684" height="402" alt="image" src="https://github.com/user-attachments/assets/a6909182-577e-4dfe-b3ae-be55e607185f" />
<img width="482" height="247" alt="image" src="https://github.com/user-attachments/assets/a2348277-2062-4732-af8c-9ba25a906ee2" />
<img width="718" height="782" alt="image" src="https://github.com/user-attachments/assets/e3befb15-3e58-4c7d-ac47-ad3b276908ac" />

**Enjoy Blackwell 🚀**
