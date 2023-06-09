# opensw23-YHL
## Team Introduction
이윤희 lylylylh

## Topic Introduction 
https://github.com/mkocabas/VIBE

video inference for human body pose and shape estimation

## Installation 
Environment : window10(x64), python 3.7, cpu only <br/>

C:/Users/(username) 안에 MOCAP 폴더를 생성하고 그 안에 VIBE 폴더를 생성한다.<br/>
	
install miniconda: <br/>
https://docs.conda.io/en/latest/miniconda.html<br/>	
-> (Windows) Miniconda3 Windows 64-bit 을 설치하고 실행한다.<br/>
  	
install VC2017 redist: <br/>
https://support.microsoft.com/pt-br/help/2977003/the-latest-supported-visual-c-downloads<br/>
-> https://aka.ms/vs/17/release/vc_redist.x64.exe 를 설치하고 실행한다.<br/>
  
download FFMPEG: <br/>
https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.zip <br/>
를 다운받아 압축을 푼 폴더를 VIBE 폴더 안에 넣는다.<br/>
  
download wget: <br/>
https://eternallybored.org/misc/wget/<br/>
wget.exe 를 다운받아 C:\Windows\System32 안에 넣는다.<br/>
      
install cuda: <br/>
https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10<br/>   
windows, X86_64, version:10, exe(local) 을 선택하여 다운로드 한다.<br/>
  
https://github.com/mkocabas/VIBE/archive/master.zip<br/>
https://github.com/carlosedubarreto/vibe_win_install/archive/main.zip<br/>
위 2개의 zip파일을 다운받아 압축을 풀고 그 안의 파일들을 VIBE 폴더 안에 넣는다.<br/>
  
anaconda prompt(miniconda3)를 실행하여 다음을 한줄씩 실행시킨다.
	
	conda create -n venv_vibe python=3.7
	conda activate venv_vibe
	conda install cudatoolkit=10.1 cudnn=7.6.0
	conda install -c anaconda git
	install_conda.bat
	prepare_data.bat
  
vibe-env\lib\site-packages\torch 폴더 내의 serialization.py 코드 내에<br/>
"map_location=NONE" 을<br/>
  	
	map_location=torch.device('cpu')
으로 바꾼다.<br/>
  
anaconda prompt(miniconda3)를 실행하여
  	
	python demo.py --vid_file sample_video.mp4 --output_folder output/ --display
을 실행한다.
  
## Results

## Analysis/Visualization
## Presentation 
