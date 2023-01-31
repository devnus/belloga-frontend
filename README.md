# Belloga Front-End
Software Maestro 13th Belloga Project Repo

### 개발 결과물

1. Web Page
    1. 토큰 재발급과 관련된 여러 번의 api 요청을 홀딩해서 순서대로 처리되도록 설정
        
        accessToken 만료에 따라 refreshToken을 통한 재발급 요청이 여러 차례 이뤄지면서 앞선 요청에서 기존의 refreshToken이 만료되어 의도치 않게 에러가 발생했습니다. 따라서 이전 요청이 완료되고 refreshToken이 갱신될때까지 잠시 다른 요청을 홀딩했습니다.
        
    2. 로딩 시 skeleton layout를 활용해서 유저가 심리적으로 느끼는 로딩 대기시간을 감축하여 사용자 경험 개선
        
        이미지를 불러올 때
        
2. Mobile App
    1. CodePush를 사용해서 업데이트 주기 단축
        
        UI 수정과 같은 사용자 피드백을 받고 즉각적으로 대응하여 업데이터 주기를 단축했습니다.
        
    2. 알람과 관련된 Android OS 기능을 분석하여 Native Module을 통해 React-Native에서 해당 기능을 사용
        
        Native Module로 Android OS의 알람 기능을 가져와 리액트 네이티브에서 사용했습니다. 알람 Schedule, 캔슬, snooze, vibration 설정 및 sound 설정이 가능합니다.
        
    3. 테스트코드 작성이 어려운 점을 보완하기 위해 [앱 배포](https://play.google.com/store/apps/details?id=com.bellogamobile) 이후 시나리오 테스트를 통해 특정 케이스에 대한 기능 작동 검증 
        
        알람 울림 및 정답 입력에 대해 단기간에 테스트코드 작성이 어려워 해당 기능들이 동작하는지에 대해 시나리오 테스트로 검증했습니다.
        

### 기술 스택

- TypeScript
- Docker
- React
- React-Native
- Tailwind
- React-Query

### 시스템 아키텍처

- Gitlab으로 형상관리
- developer ⇒ gitlab ⇒ ecr ⇒ ec2로 도커로 배포

### 실행 방법

1. 개발 환경
    1. React
        
        Node: 16.13.2
        
        React: 17
        
    2. React-Native
        
        JDK : `Zulu11`
        
        Node: `16.13.2`
        
        React Native: `0.66.4`
        
        React: `17.0.2`
        
    
2. 실행
    1. react
        
        ```
        npm install
        npm start
        ```
        
  <p align="center"> <img width="300" alt="bellogaImg" src="https://user-images.githubusercontent.com/80435616/215764372-fcd30fb5-2bd7-4acb-9b97-1327d5497775.png">

    
 </p>

    *This Project is Sponsored by **Software Maestro***
    
    This work was supported by the Institute of Information & Communications Technology Planning & Evaluation(IITP) grant funded by the Ministry of Science and ICT(MSIT) (IITP-2022-SW Maestro training course).
