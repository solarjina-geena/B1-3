
## 프로젝트 1 

 동일한 워크플로우를 **Make.com**과 **Zapier** 2개 도구로 구현 후 비교



```
[Google Form 제출]
        ↓ Trigger
[심각도 조건 분기] ← Router/Filter
    ↓ 
[ Discord 알림]
    ↓                   
[심각도 상 시트 기록]  

```

---

### 📍 Make.com 구현 순서

```
<img width="1525" height="684" alt="01 MAKE FLOW-1" src="https://github.com/user-attachments/assets/e6c0d605-6377-4e61-8d64-34fb806e3886" />


모듈 추가
  - Google Forms → Watch Responses (Trigger)
  - Router 추가 (심각도)
  - Action 1:  Discord 알림
  - Action 2 : 구글시트 리스트 작성
 

구글폼 제출
<img width="512" height="607" alt="02 구글폼" src="https://github.com/user-attachments/assets/8310f900-17df-4381-9612-0f697ce2928c" />


구글폼 응답
<img width="1251" height="341" alt="03 구글시트 응답" src="https://github.com/user-attachments/assets/231620b2-e968-4ec7-ade9-80b97371ba0d" />


경로1 심각도 상
  Discord 알림
<img width="518" height="107" alt="04 디스코드 알람" src="https://github.com/user-attachments/assets/0130e2fd-c046-4de6-98a3-b933cf495092" />

 
Action 2 심각도 상 구글시트 작성
<img width="724" height="584" alt="05 MAKE 심각도 상 구글시트" src="https://github.com/user-attachments/assets/27404eea-75a1-47dc-8e6e-af434880f77b" />

```

---

### 📍 Zapier 구현 순서

```
<img width="583" height="847" alt="06 ZAPIER FLOW 2" src="https://github.com/user-attachments/assets/15f0cbd2-4bfe-4cb6-b217-ee9eeebe6f1d" />

  - Trigger: Google Forms → 사진수집 구글시트 동일하게 사용, "자피어" 탭추가하여 응답
  - Filter: 조건 설정 (심각도 상)
  - Action 1: Google Sheets
<img width="1120" height="481" alt="07자피어 구글시트2" src="https://github.com/user-attachments/assets/a18a6f10-c6ba-4ba2-b9bc-a8d0ceeb323d" />


  - Action 2: Discord 알림
<img width="966" height="661" alt="08 ZAPIER 메세지2" src="https://github.com/user-attachments/assets/b172a386-2bbd-4d25-bd2c-17ebc22fc085" />


```

---

### 📊 비교 분석 보고서 작성 


## 비교표
<img width="1002" height="585" alt="09 MAKE ZAPIER 비교분석" src="https://github.com/user-attachments/assets/a97ebdd9-d19b-445f-84d6-8db2ec83152e" />


## 장단점 요약
### Make
- 장점: 복잡한 분기 설계 가능, 무료 Ops 넉넉
- 단점: 초보자 진입장벽 있음

### Zapier
- 장점: 직관적 UI, 연동 앱 많음
- 단점: 무료 플랜 제한 적음

## 도구 선택  : 직관적으로 작업하기 쉽고, 무료로 사용가능 빈도가 더 제공되어 MAKE 를 사용
---

## 프로젝트 2 - 불량 관리 자동화 🏭

---

### 🔧 워크플로우 설계

```
[현장 작업자가 Google Form으로 불량 정보 입력]
  - 불량 사진 첨부
  - 불량 유형 선택 (균열/변색/파손 등)
  - 발생 위치 입력
  - 심각도 선택 (상/중/하)
        ↓ Trigger (Form 제출)
        
[조건 분기: 심각도 기준]
    ↓               ↓
[심각도 "상"]    [심각도 "중/하"]
    ↓               ↓
[긴급 이메일     [일반 Sheets
 알림 발송]       기록만]
    ↓
[Google Sheets 불량 대장 자동 기록]
  - 날짜/시간 자동 입력
  - 사진 링크 자동 연결
  - 불량 유형/심각도 기록
```
   불량내용에 대해서 확장성 가능
   작업자들의 불량 이미지 공유 만으로 실시간 공정관리 가능
---

```

### 프로젝트 2 ✅
```
□ 반복 업무 정의 작성 :일일 공정불량 확인
□ 도구 선정 이유 작성 : 불량단계로 분리해서 리스트 업 해야하는데,
    make 가 action은  문어발식으로 확장할 수 있어서 선택
□ 워크플로우 흐름 
<img width="695" height="572" alt="201 MAKE FLOW" src="https://github.com/user-attachments/assets/b9bd2b5a-5dc4-4aa1-a2f9-ff2008b1c861" />

□ 실행 결과
  디스코드
<img width="514" height="230" alt="image" src="https://github.com/user-attachments/assets/d844c968-7376-476c-b038-b21a1241002e" />

  심각도 상
<img width="551" height="701" alt="image" src="https://github.com/user-attachments/assets/96d2b9af-3d8f-40a8-a053-e7493c0651e0" />

  심각도 중/하
<img width="609" height="585" alt="202 메이크 심각도 중 하 구글시트" src="https://github.com/user-attachments/assets/f3a53ae5-2392-4d16-9415-e029df8a8be7" />

□ Trigger 자동 실행 확인
```

구글시트 [text](https://docs.google.com/spreadsheets/d/1y9qPMGppHI0Mu6x6hze-oQG3AjvWdpVUp1YR5mkaN3M/edit?usp=sharing)

구글폼 https://forms.gle/Vio9fVNkiPVNhQhKA

메이크 https://eu1.make.com/2159956/scenarios/6607535/edit

자피어 https://zapier.com/editor/374019374/draft
