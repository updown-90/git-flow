# git-flow

팀에 git-flow를 도입하고자 테스트하려고 만든 Repo

## 목적
* 현재 저희 팀에서 여러 가지 형태의 업무(티켓)이 만들어지고 있고 큰 규모의 개발 건들도 많이 들어와 약 1달 이상 들고 있는 티켓 들고 다수로 많아지고 있어 이런 프로세스를 가장 잘 반영할 수 있는 브랜치 전략이 Git flow라고 생각해 전략을 수립

## 설명
* master : 제품으로 출시될 수 있는 브랜치
* develop : 다음 출시 버전을 개발하는 브랜치
* feature : 기능을 개발하는 브랜치
* release : 이번 출시 버전을 준비하는 브랜치
* hotfix : 출시 버전에서 발생한 버그를 수정 하는 브랜치
* ![image](https://user-images.githubusercontent.com/52308702/200251251-bcdf818d-4a81-4602-911a-74268aa76fc6.png)


## 방법
1. 티켓을 배정받고 develop 기준으로 feature/xxx 브랜치를 생성한다
2. feature/xxx에서 개발이 완료되면 develop에 PR을 올리고 승인받고 머지하고 feature/xxx 브랜치는 제거
3. 2번에서 완료된 develop 기준으로 release 브랜치를 생성한다
4. release 브랜치 기준으로 태그 생성해서 stg에 올려 QA 진행
5. 완료되면 release 브랜치를 develop과 master 브랜치에 머지하고 태그 생성해서 배포

## 참고
* https://techblog.woowahan.com/2553/
* https://danielkummer.github.io/git-flow-cheatsheet/index.ko_KR.html
