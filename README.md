# git-flow-training

### 💡  문제 조건

- merge한 branch는 삭제할 것
- merge 이후에도 git flow가 남도록 merge시 `--no-ff` 옵션을 사용할 것
- 모든 작업이 끝난 후 graph로 출력 되도록 하고, 예시와 같은 플로우가 되도록 할 것

### ✔ 최종 git log

![image](https://user-images.githubusercontent.com/96973332/186093212-b5951ca1-4b3c-4632-ae31-341001b6921f.png)

# 💡  release, hotfix, feature에 대한 깨알 지식

### release

바로 배포할 것이 아닌,  앞으로 배포할 내용에 대해 `releases branch`에 두고 작업한다.

- 실제 기능 개발은 `develop/feature/기능명` 에서 진행
- 출시 준비는 `release/버젼` 에서 develop 의 내용을 머지하며 업그레이드 시킨다.
- `master` 는 언제든 실행 가능한 상태를 유지해야하기 때문에 앞으로의 배포 상태를 위한 파일은 release에 둔다.

master에 merge 시 **--no -ff** 를 진행할 것을 추천 (병합을 위한 커밋 기록을 의도적으로 남기는 방법)
 <br> <br>
### hotfix

<b> hotfix 브랜치를 만드는 경우 ? </b>

배포대상인 master 브랜치 작업물에 **긴급히 수정해야하는 내용**이 있을 때, 
**master 브랜치에서 바로 브랜치를 열어 수정사항을 반영하는 것**이다.
 <br> <br>
### 유지 브랜치와 보조 브랜치

- **항상 유지가 되는 메인 브랜치**
    - **master** : 현재 바로 실행가능한 제품 브랜치
    - **develop** : 다음 출시 버젼을 개발하는 브랜치
- **보조 브랜치**
    - **release** : 다음 출시 버젼을 준비하는 브랜치
    - **feature** : 기능 구현 브랜치
    - **hotfix** : master의 내용에서의 버그를 긴급히 수정하는 브랜치
    
     <br> 
# 💡  --no-ff, ff란?
- `--no-ff` : 병합 대상 브랜치가 fast-forward 관계인 경우에도 반드시 병합 커밋을 만든다. <br>
Ex) `git merge --no-ff [branch]
- <b> fast-forward (-ff) ? </b> <br>
   두 개의 커밋A와 커밋B가 존재할 때 커밋B의 히스토리에 커밋A의 커밋 히스토리가 포함되어 있을 경우, 커밋 A는 커밋B에 Fast-Forward 한다고 표현한다.
    <br> <br>
---

<b> [ reference ] </b> <br>
release, hotfix, feature에 대한 출처 : 
[브랜치 관리를 위한 git-flow](https://velog.io/@skawnkk/%EB%B8%8C%EB%9E%9C%EC%B9%98-%EA%B4%80%EB%A6%AC%EB%A5%BC-%EC%9C%84%ED%95%9C-git-flow)
