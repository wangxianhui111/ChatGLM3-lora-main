# ChatGLM3-Lora

ChatGLM3自我认知微调


准备好数据集

## 数据集格式

![数据集格式图](./image/1.png)

运行transdata
对数据集进行格式转换符合ChatGLM3的格式
![数据集转换后图](./image/4.png)

## 进行微调训练
利用LLama_factory进行微调
微调参数设置：
    --stage sft \
    --do_train \
    --dataset self_cognition \
    --finetuning_type lora \
    --output_dir cognition \
    --overwrite_cache \
    --per_device_train_batch_size 2 \
    --gradient_accumulation_steps 2 \
    --lr_scheduler_type cosine \
    --logging_steps 10 \
    --save_steps 1000 \
    --warmup_steps 0 \
    --learning_rate 1e-3 \
    --num_train_epochs 10.0 \
## 微调结果
### 微调前
![结果图](./image/2.png)
### 微调后
![结果图](./image/3.png)


