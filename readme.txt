下载 https://github.com/TencentARC/GFPGAN/releases/download/v1.3.0/GFPGANv1.4.pth

复制或移动下载好的NovelAI模型到项目文件夹 stable-diffusion-webui

复制GFPGANv1.4.pth 到 stable-diffusion-webui 根目录。
复制novelaileak\stableckpt\animefull-latest\model.ckpt 到 stable-diffusion-webui\models\Stable-diffusion目录下，并改名为final-pruned.ckpt, 可能有同学会问，为什么是这个模型，我只能告诉你，这是成年人的快乐 ：）。
复制novelaileak\stableckpt\animefull-latest\config.yaml 到 stable-diffusion-webui\models\Stable-diffusion目录下，并改名为final-pruned.yaml 。
复制novelaileak\stableckpt\animevae.pt 到 stable-diffusion-webui\models\Stable-diffusion目录下，并改名为final-pruned.vae.pt 。
复制novelaileak\stableckpt\modules\modules下的所有文件 到 stable-diffusion-webui\models\hypernetworks目录下，如果hypernetworks目录不存在，新建文件夹即可。

python launch.py --server_name 192.168.10.18

遇到 module 'cv2.cv2' has no attribute 'FaceDetectorYN'
pip uninstall opencv-python-headless
pip uninstall opencv-python
pip install opencv-contrib-python
