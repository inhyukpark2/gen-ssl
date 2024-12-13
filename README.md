## Generative Self-Supervised Learning for Medical Image Classification

<b>Generative Self-Supervised Learning for Medical Image Classification</b><br/>
Inhyuk Park, Sungeun Kim, Jongbin Ryu.<br/> 
(Asian Conference on Computer Vision <b>(ACCV)</b>, 2024) <br/>

<img src="GenSSL.png" alt="model overview" width="100%">

## Generative Chest X-ray Images 
After training the generative model, generate a chest x-ray image. [generative_chestxray](https://github.com/Warvito/generative_chestxray)

## Pre-training on generated Chest X-ray Images

The pre-training instruction is in [PRETRAIN.md](https://github.com/inhyukpark2/gen-ssl/blob/main/PRETRAIN.md).

## Fine-tuning with pre-trained checkpoints

The fine-tuning instruction is in [FINETUNE.md](https://github.com/inhyukpark2/gen-ssl/blob/main/FINETUNE.md).

## Acknowledgement
We referenced the implementation of [medical_mae](https://github.com/lambert-x/medical_mae)

## Future works
We plan to conduct further studies to develop a more powerful diffusion model, generate a larger number of high-quality images, and explore more effective self-supervised learning methods.👨🏻‍💻
