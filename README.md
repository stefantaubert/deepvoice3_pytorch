python preprocess.py ljspeech --preset=presets/ljspeech-lite.json /datasets/LJSpeech-1.1-lite /datasets/preprocessed/ljspeech-lite

python train.py --preset=presets/ljspeech-lite.json --data-root=/datasets/preprocessed/ljspeech-lite

python synthesis.py ./checkpoints/checkpoint_step000000838.pth ./examples/synthesize.txt ./examples/wav --preset=presets/ljspeech-lite.json