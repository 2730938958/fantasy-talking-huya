海聪镜像：registry-haiyan.local.huya.com/machine-learn/fengweiyan_fantasytalking:cuda12

模型下载命令：
pip install modelscope
modelscope download Wan-AI/Wan2.1-I2V-14B-720P --local_dir ./models/Wan2.1-I2V-14B-720P
modelscope download AI-ModelScope/wav2vec2-base-960h --local_dir ./models/wav2vec2-base-960h
modelscope download amap_cvlab/FantasyTalking   fantasytalking_model.ckpt  --local_dir ./models


更改infer.py / app.py 的wan和wav2vec的路径

推理命令：
python infer.py  --image_path ./assets/images/woman.png --audio_path ./assets/audios/woman.wav --prompt "The person is speaking enthusiastically, with their hands continuously waving." --prompt_cfg_scale 5.0 --audio_cfg_scale 5.0

gradio：
python app.py
