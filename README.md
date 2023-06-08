# opensw23-YHL
Team Introduction: 이윤희 lylylylh
Topic Introduction: 
  video inference for human body pose and shape estimation
  (영상 속 사람의 움직임을 포착하여 동작과 형태를 추정하고 이를 바탕으로 새 영상을 만들어낸다.)
Results: empty 
Analysis/Visualization: 
Installation: 
  < environment - window10(x64), python 3.7, cuda 10.1, cpu only >
  C:/Users/(username) 안에 MOCAP 폴더를 생성하고 그 안에 VIBE 폴더를 생성한다.
  install miniconda: https://docs.conda.io/en/latest/miniconda.html
                      -> (Windows)	Miniconda3 Windows 64-bit 을 설치하고 실행한다.
  install VC2017 redist: https://support.microsoft.com/pt-br/help/2977003/the-latest-supported-visual-c-downloads
                      -> https://aka.ms/vs/17/release/vc_redist.x64.exe 를 설치하고 실행한다.
  download FFMPEG: https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.zip 
  를 다운받아 압축을 푼 폴더 VIBE 폴더 안에 넣는다.
  download wget: https://eternallybored.org/misc/wget/
                       wget.exe 를 다운받아 C:\Windows\System32 안에 넣는다.
  
  https://github.com/mkocabas/VIBE/archive/master.zip
  https://github.com/carlosedubarreto/vibe_win_install/archive/main.zip
  위 2개의 zip파일을 다운받아 압축을 풀고 그 안의 파일들을 VIBE 폴더 안에 넣는다.
  
  anaconda prompt(miniconda3)를 실행하여 아래 6줄을 1줄씩 실행시킨다.
  conda create -n venv_vibe python=3.7
  conda activate venv_vibe
  conda install cudatoolkit=10.1 cudnn=7.6.0
  conda install -c anaconda git
  install_conda.bat
  prepare_data.bat
  
  vibe-env\lib\site-packages\torch\serialization.py를 실행하여
  "map_location=NONE" 을
  "map_location=torch.device('cpu')" 으로 바꾼다.
  
  anaconda prompt(miniconda3)를 실행하여
  python demo.py --vid_file sample_video.mp4 --output_folder output/ --display
  을 실행한다.
  
Presentation: 
