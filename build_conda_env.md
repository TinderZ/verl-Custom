# verl 环境搭建指南

## 1. 创建环境

```bash
conda create --name verl python==3.10
conda activate verl
```

## 2. clone verl框架

```bash
git clone https://github.com/volcengine/verl
cd verl
pip3 install -e.
```

## 3. 安装依赖（顺序不要错）

```bash
pip install vllm==0.8.2
pip install tensordict==0.6.2
pip install "sglang[all]>=0.4.5.post3"
pip install torch==2.6.0 torchaudio==2.6.0 torchvision==0.21.0
pip install ray==2.44.0
```

## 4. 注意flash-attn==2.6.3一定要去github上下载，选择上选择False

下载地址：https://github.com/Dao-AILab/flash-attention/releases/tag/v2.6.3

选择文件：
```
flash_attn-2.6.3+cu123torch2.4cxx11abiFALSE-cp310-cp310-linux_x86_6
```

安装命令：
```bash
pip install 安装包目录
```

## 版本检查

安装好后检查一下，几个重要的依赖版本：
- cuda==12.4
- python==3.10
- vllm==0.8.2
- flash-attn==2.6.3
- torch==2.6.0