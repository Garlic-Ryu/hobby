# 내과학 각 과, 하루 1개 한의학 처방 데이터 
이 프로젝트는 한국한의학연구원에서 제공하는 한의대 내과학 교과서 데이터를 분석하여, 처방과 관련된 증상 및 설명을 추출하는 데 사용됩니다. 
각 처방은 간계, 심계, 비계, 폐계, 신계 내과학 분야로 구분되며, 각 분야별로 한 개의 처방과 그에 따른 증상 및 설명을 랜덤으로 추출합니다.

## 시작하기 전에
한의학연구원에서 공개하는 처방 데이터를 이용하였습니다. 각 파일에는 해당하는 내과학 분야의 처방명, 증상명이 기재되어있습니다.
증상명이 없는 경우는 제외하였습니다.
- 한국한의학연구원_한의대 간계내과학 교과서 처방 데이터_20230816.csv
- 한국한의학연구원_한의대 심계내과학 교과서 처방 데이터_20230816.csv
- 한국한의학연구원_한의대 비계내과학 교과서 처방 데이터_20230816.csv
- 한국한의학연구원_한의대 폐계내과학 교과서 처방 데이터_20230816.csv
- 한국한의학연구원_한의대 신계내과학 교과서 처방 데이터_20230816.csv

각 파일은 해당하는 내과학 분야의 처방 데이터를 포함하고 있습니다.

## 파일 업로드
Google Colab을 사용하여 프로젝트를 실행할 경우, 먼저 위의 데이터 파일을 Colab에 업로드해야 합니다. 이는 다음 코드를 통해 수행할 수 있습니다:

```python
from google.colab import files
uploaded = files.upload()

## 실행 예시
1회차
'(간계) 천진원', [['비신구허', '비와 신이 모두 허해진 것'], ['음식부진', '식욕이 없는 것'], ['진액고갈', '진액(津液)이 고갈되는 것']]
'(심계) 영양각탕', [['간양상항', '간신음허(肝腎陰虛)로 간양(肝陽)을 제어하지 못하여 양기(陽氣)가 지나치게 상승한 병리상태(病理狀態)'], ['신음허', '신(腎)의 음기(陰氣)가 부족한 상태로, 정(精)을 상하거나 진액(津液)이 모손되거나 급성열병으로 신음(腎陰)을 손상하여 발생하는 병증']]
'(비계) 측백산', [['구비개류', '입과 코에서 모두 분비물(피)이 흐름'], ['기출여용천', '그 나오는 것이 용솟는 샘물과 같음'], ['내손심폐', '내부(內部)가 심(心)과 폐(肺)를 손상한 것'], ['토혈하혈', '피를 토하고 하혈하는 것']]
'(폐계) 천영개산', [['채충', '노채로 인해 생긴 충(蟲)을 없앤다']]
'(신계) 고암심신환', [['각위', '다리가 약하고 힘이 없는 증상으로 심하면 근육이 위축되는 병'], ['경계', '갑자기 가슴이 뛰어서 의식을 잃고 쓰러질 듯한 병증'], ['노손심신', '노상(勞傷)으로 인해 심(心)과 신(腎)이 손상된 상태'], ['도한', '야간에 자는 동안 땀이 나지만 느끼지 못하고 깨어나면 땀이 그치는 것'], ['목암', '눈이 어두워지는 것'], ['요통', '허리가 아픈 것'], ['유정', '정액이 저절로 나오는 병증'], ['이명', '귀에서 이상한 소리가 나는 것'], ['정충', '가슴이 몹시 두근거리는 병증']]
