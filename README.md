# Neural Sparse Representation for Image Restoration

Preprint [[arXiv]](https://arxiv.org/abs/2006.04357)

## Usage

Clone our [Image Restoration Toolkit](https://github.com/ychfan/pt_ir) and install [dependencies](https://github.com/ychfan/scn#dependencies).
```bash
git clone --recurse-submodules https://github.com/ychfan/pt_ir.git
```

## Performance

### Image super-resolution

Small models

| Networks | Parameters | DIV2K (val) | Set5 | B100 | Urban100 | Manga109 | Pre-trained | Eval cmd | Train cmd |
| - | - | - | - | - | - | - | - | - | - |
| EDSR+NSR x2 | 4,877,812 | 34.87 | 38.11 | 32.22 | 32.58 | 38.95 | [Download](https://drive.google.com/file/d/172LBsecM6LIG6OF9QY5MKCD9wUt7OZpP/view?usp=sharing) | <details><summary>details</summary>```python trainer.py --eval_only --dataset div2k --eval_datasets div2k set5 bsds100 urban100 manga109 --scale 2 --model wdsr_nsr --num_blocks 16 --num_residual_units 64 --width_multiplier 1 --num_sparsity_groups 4 --job_dir X --ckpt ./logs/edsr_s_nsr_x2/epoch_30.pth```</details> | <details><summary>details</summary>```python trainer.py --dataset div2k --eval_datasets div2k set5 bsds100 urban100 manga109 --scale 2 --model wdsr_nsr --num_blocks 16 --num_residual_units 64 --width_multiplier 1 --num_sparsity_groups 4 --job_dir ./logs/edsr_s_nsr_x2```</details> |
| EDSR+NSR x3 | 4,887,637 | 31.10 | 34.50 | 29.14 | 28.45 | 33.76 | [Download](https://drive.google.com/file/d/1bhc55AKRX80Gf4n3LbofE70aRCn0zobr/view?usp=sharing) | <details><summary>details</summary>```python trainer.py --eval_only --dataset div2k --eval_datasets div2k set5 bsds100 urban100 manga109 --scale 3 --model wdsr_nsr --num_blocks 16 --num_residual_units 64 --width_multiplier 1 --num_sparsity_groups 4 --job_dir X --ckpt ./logs/edsr_s_nsr_x3/epoch_30.pth```</details> | <details><summary>details</summary>```python trainer.py --dataset div2k --eval_datasets div2k set5 bsds100 urban100 manga109 --scale 3 --model wdsr_nsr --num_blocks 16 --num_residual_units 64 --width_multiplier 1 --num_sparsity_groups 4 --job_dir ./logs/edsr_s_nsr_x3```</details> |
| EDSR+NSR x4 | 4,901,392 | 29.10 | 32.26 | 27.61 | 26.18 | 30.62 | [Download](https://drive.google.com/file/d/17fL34RTCPWCvfCqmSZfLr1k8nM8PT5QB/view?usp=sharing) | <details><summary>details</summary>```python trainer.py --eval_only --dataset div2k --eval_datasets div2k set5 bsds100 urban100 manga109 --scale 4 --model wdsr_nsr --num_blocks 16 --num_residual_units 64 --width_multiplier 1 --num_sparsity_groups 4 --job_dir X --ckpt ./logs/edsr_s_nsr_x4/epoch_30.pth```</details> | <details><summary>details</summary>```python trainer.py --dataset div2k --eval_datasets div2k set5 bsds100 urban100 manga109 --scale 4 --model wdsr_nsr --num_blocks 16 --num_residual_units 64 --width_multiplier 1 --num_sparsity_groups 4 --job_dir ./logs/edsr_s_nsr_x4```</details> |
