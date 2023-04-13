# KcELECTRA를 황용한 '저희' 의미 분류기

<!--- These are examples. See https://shields.io for others or to customize this set of shields. You might want to include dependencies, project status and licence info here --->
## Dataset
연세 말뭉치와 위키 문헌 근대 문학에서 '저희'가 포함된 문장을 '지칭의 저희'(label 0)와 '겸양의 저희(label 1)'로 분류

1. transformer 와 HuggingFace 를 이용하여 Beomi님의 KcELECTRA(https://github.com/Beomi/KcELECTRA)를 통해 '저희'의 의미를 이진분류하는 모델 생성 ('지칭의 저희'(label 0)와 '겸양의 저희(label 1)'로 분류)
2. 만든 모델로 조선일보, 동아일보 100년 데이터에서 '저희'의 의미 분류
3. Explainable AI SHAP(https://shap.readthedocs.io/en/latest/index.html) 모델을 활용하여 각 분류에 유의미하게 쓰인 단어 확인

## Prerequisites

Before you begin, ensure you have met the following requirements:
<!--- These are just example requirements. Add, duplicate or remove as required --->
* You have installed the 3.9X version of `Python`.
* Install packages with requirements.txt
```
$ pip install -r requirements.txt
```## 

## 코드

1. KcELECTRA_모델_fine_tuning_조선동아_기사_분류.ipynb 
Finetuning dataset(train_small.csv, test_small.csv)을 불러와서 '저희'의미 분류 모델 Finetuning
Finetuning된 모델로 조선, 동아일보의 '저희'가 포함된 문장 이진분류
시계열로 의미 활용 추세 그래프 제작

2. KcELECTRA_모델_SHAP.ipynb
기학습된 모델이 의미를 분류하는데에 중요하게 판단한 단어들을 찾기 위해
Explanable AI SHAP 모델을 활용

## Contributing to <project_name>
<!--- If your README is long or you have some specific process or steps you want contributors to follow, consider creating a separate CONTRIBUTING.md file--->
To contribute to <project_name>, follow these steps:

1. Fork this repository.
2. Create a branch: `git checkout -b <branch_name>`.
3. Make your changes and commit them: `git commit -m '<commit_message>'`
4. Push to the original branch: `git push origin <project_name>/<location>`
5. Create the pull request.

Alternatively see the GitHub documentation on [creating a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).


## Contact

If you want to contact me you can reach me at <david1224@g.skku.edu>.
