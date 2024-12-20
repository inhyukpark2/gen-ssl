## Fine-tuning Pre-trained ViTs

##### Fine-tune ViTs

Script example for ViT-S pretrained on generated Chest X-ray Images, with **single-node training**, run the following on 1 node with 8 GPUs:

```
OMP_NUM_THREADS=1 python -m torch.distributed.launch \
    --nproc_per_node=8 \
    --use_env main_finetune_chestxray.py \
    --output_dir ${SAVE_DIR} \
    --log_dir ${SAVE_DIR} \
    --batch_size 128 \
    --finetune "your_model.pth" \
    --epochs 75 \
    --blr 2.5e-4 --layer_decay 0.55 --weight_decay 0.05 \
    --model vit_small_patch16 \
    --warmup_epochs 5 \
    --drop_path 0.2 --mixup 0 --cutmix 0 --reprob 0 --vit_dropout_rate 0 \
    --data_path ${DATASET_DIR} \
    --num_workers 4 \
    --train_list ${TRAIN_LIST} \
    --val_list ${VAL_LIST} \
    --test_list ${TEST_LIST} \
    --nb_classes 14 \
    --eval_interval 10 \
    --min_lr 1e-5 \
    --build_timm_transform \
    --aa 'rand-m6-mstd0.5-inc1'
```
