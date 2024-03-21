# download code
git clone https://github.com/SWALLOWhajnal/VrtDi.git

cd VrtDi

pip install -r requirements.txt

##e.g. 001:  video sr trained on REDS (6 frames),   -pretrain-model:team_40_VRT.pth

python main_test_vrt.py --task 001_VRT_videosr_bi_REDS_6frames  --folder_lq=<data_dir>/DIV2K_LSDIR_valid_LR  --tile 40  128 128 --tile_overlap 2 20 20 --save_result --num_workers=4

##e.g. 002:

python main_test_vrt.py --task 001_VRT_videosr_bi_REDS_6frames --folder_lq=<data_dir>/DIV2K_LSDIR_valid_LR --folder_gt=<data_dir>/DIV2K_LSDIR_valid_HR --tile 
10 256 256 --tile_overlap 2 20 20 --num_workers=4

