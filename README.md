# 依存ライブラリのインストール

```
pip install torch==1.13.1 torchvision==0.14.1 torchaudio==0.13.1 --extra-index-url https://download.pytorch.org/whl/cu11

git submodule update --init --recursive
pip install -r requirements.txt
pip install 'git+https://github.com/facebookresearch/detectron2.git'
```

# デモコード実行例

```
cd DiffMatte
python run_one_image.py \
    --config-file ViTS_1024 \
    --checkpoint-dir ../checkpoints/DiffMatte_ViTS_Com_1024.pth \
    --image-dir demo/retriever_rgb.png \
    --trimap-dir demo/retriever_trimap.png \
    --output-dir ../result2.png \
    --device cuda \
    --sample-strategy ddim10
```

# 参考 issue

- <https://github.com/YihanHu-2022/DiffMatte/issues/5>
