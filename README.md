# opensw23-YHL
## Team Introduction
이윤희 lylylylh

## Topic Introduction 
https://github.com/mkocabas/VIBE

video inference for human body pose and shape estimation

## Installation 
Environment : window10(x64), cpu only <br/>
> python == 3.7<br/>
> tensorboard == 1.15.0 <br/>
> tensorflow == 1.15.4 <br/>
> torch == 1.4.0+cu92 <br/>
> torchvision == 0.5.0+cu92 <br/>
> pyglet == 1.4.10<br/>
> PyOpenGL == 3.1.0<br/>
> opencv-python == 4.1.2.30<br/>

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
  
anaconda prompt(miniconda3)를 실행하여 다음을 실행시킨다.
	
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

(input).mp4 파일을 VIBE 폴더 안에 넣는다. <br/>

anaconda prompt(miniconda3)를 실행하여
  	
	python demo.py --vid_file (input).mp4 --output_folder output/ --display
을 실행한다.
  
## Results
<Sample Video><br/>
	

https://github.com/lylylylh/opensw23-YHL/assets/117340443/83e05c5e-fd32-4ec4-8d51-25332020aded


<Video1><br/>


https://github.com/lylylylh/opensw23-YHL/assets/117340443/e22a1ec5-e678-4b9a-a572-b0d7bca50620
	
	
	

<Video2><br/>			
	
	

https://github.com/lylylylh/opensw23-YHL/assets/117340443/948190fa-a7a6-4785-a5a9-e9c34129c9e3


	
<Video3><br/>	
	
	

https://github.com/lylylylh/opensw23-YHL/assets/117340443/61637dbb-c8c1-46f2-a537-3a3526ebd3d0


	
	
## Analysis/Visualization
sample video의 결과를 보면 input영상의 신체가 겹치지 않고 움직임을 명확하게 포착할 수 있기 때문에 결과가 잘 나타나는 것을 볼 수 있지만 video1의 결과에 보면 신체가 겹치거나 특정 신체 부위가 영상에서 사라졌다가 나타나거나 빠르게 움직이는 부분에서 불안정한 것을 볼 수 있다. 또한 특히나 손의 위치와 모양, 손가락의 모양의 정확한 추정이 잘 시행되지 않고 있다.<br/>
또한 video2의 결과를 보면 video1과 비교하였을때 인원 수가 1명에서 5명으로 증가하였지만 각 사람 사이에 공간이 존재하고 위치가 겹치지 않는다면 sample video처럼 움직임을 정확하게 포착하는 것을 볼 수 있다. 그러나 사람이 둘 이상 위치가 겹쳐 신체가 겹치거나 움직임이 영상에 가려져서 나타나거나 하는 경우에는 결과가 불안정하다.<br/>
video3의 결과를 보면 video2와 인원 수도 같고 위치 또한 겹치지 않으며 움직임도 같지만 배경과 사람의 구분이 잘 이루어지지 못했기 때문에 결과가 거의 도출되지 않는다. 그러므로 사람을 제외한 뒷배경이 프로그램 실행에 중요한 요소 중 하나임을 알 수 있다.<br/>
## Presentation 
