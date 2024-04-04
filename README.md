## 🤪 Emopic: 텍스트 감정분석에 따른 표정 이미지 변환 서비스
**내용** 
- 텍스트 감정 분석을 통해 사진 속 얼굴 표정을 변경하는 서비스 개발. 텍스트에서 감정을 분석해 여섯 가지 카테고리로 분류한 후, StarGan 모델을 사용해 해당 감정에 맞게 사진의 표정을 변환함.

**프로젝트 기간**: 2023.07.15 ~ 2023.08.30

**팀 구성**: 멀티캠퍼스 데이터분석&엔지니어 과정_4인팀

**역할** `기여도 35%`
- 대시보드 시각화
- 다중감정분류 모델 제작
- 장고 모델 연결

**스킬**

Python, pandas, sklearn, Kobert, StarGan, Django

**데이터수집**

- [AI허브] [감정분류를 위한 대화 음성 데이터셋](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&dataSetSn=263)
- [AI허브] [한국인 감정인식을 위한 복합 영상](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&dataSetSn=82)

**배운점**

- 텍스트와 이미지 데이터의 증강 및 전처리 경험 얻음.
- 주제 선정부터 시장조사, 논문 리뷰, AI 서비스의 웹 구현에 이르기까지 서비스기획 전 과정을 체계적으로 경험.
- 다양한 라이브러리를 사용하면서 의존성 문제를 경험하고 호환성 및 의존성 관리의 중요성을 느낌.

![example](images/example.png)



 EmoPic is combined by two words, **emo**tion + **pic**ture. EmoPic is a service which make changes in facial expressions through Korean text sentiment analysis. The sentiment analysis of Korean text is done by KoBert. The StarGan model is used for making facial expressions changes in pictures.

 Getting two inputs, text from utterance and a portrait photo, the EmoPic service categorizes the emotion implied in the input text in 6 different categories, then photoshops the input picture changing the face expression to the analyzed sentiment.

 Text sentiment analysis model is trained my utterance text and face expression changing model is trained by selfies of Koreans with various categories.

KoBert : https://github.com/SKTBrain/KoBERT

StarGan : https://github.com/yunjey/stargan

Team Levelup : [Kyeongwon Cho](https://github.com/F1RERED), [Youkyung Kang](https://github.com/KYK0328), [Taeyoung Kim](https://github.com/xaeyoungkim), [Hyoeun Lee](https://github.com/hyony2)

--------------

## Demonstration videos

<Data dashboard & Login & Signup>

https://github.com/F1RERED/EmoPic/assets/135773973/61e93ffb-eebf-42d3-9059-8b8cae0773e1

<Direct inputs & slang [Surprised]>

https://github.com/F1RERED/EmoPic/assets/135773973/c775bf38-3f76-487d-9bf8-3b71bc36df8a

<Using image2text(Naver Cloud OCR) API & screenshotlayer API [Sad]>

https://github.com/F1RERED/EmoPic/assets/135773973/099ccba4-24fc-425c-a9f8-05e704d2452c

<Distribution server(gunicorn & nginx)  [Angry])>

https://github.com/F1RERED/EmoPic/assets/135773973/8d35bc2f-85db-4c64-b293-568a52f172af

--------------------------------

## Files to be replaced

```
EmoPic

 └ mysite

	 └ .cache

		 └ kobert_v1.zip

	└ mysite

		└ surprise.pt


	└ stargan

		└ models

			└ 300000-D.ckpt

			└ 300000-G.ckpt

```

* kobert_v1.zip

  should be the trained model of kobert

+ surprise.pt

  should be the trained model of sentiment analysis based on kobert

+ 300000-D.ckpt & 300000-G.ckpt 

  should be the trained model of stargan 

-------

## API keys

* edit your views.py

service_view_naver_OCR_api_url = # Place your API keys here
service_view_naver_OCR_secret_key = # Place your API keys here

get your API key from this link :

https://www.ncloud.com/product/aiService/ocr



screenshotlayer_capture_screenshot_api_key = # Place your API keys here

get your API key from this link :

https://screenshotlayer.com/



service_result_view_removebg_API_key = # Place your API keys here

get your API key from this link :

https://www.remove.bg/ko



-------------------------

## Requirements

 Simulation based on python 3.7

 Versions in [requirements.txt](requirements.txt) are not mandatory. It's only the version used for our project.

 Please refer to the KoBert's and the StarGan's dependecies.

---------------------------------

## etc.

![certificate](images/[D27]_상장(문제해결빅데이터활용프로젝트)_최우수상_3조.jpg)
