# Git guideline


## Git-Flow

Git-Flow를 사용해 유연한 프로덕트 관리를 돕습니다.

기본적으로 2개의 브랜치를 유지합니다.(master, develop)

- **master:** Release 되어 출시될 제품의 브렌치 (라이브 서버는 해당 브렌치를 바라봅니다)
- **develop:** 다음 버전을 현재 개발중인 브랜치

추가적으로 유연하게 브랜치를 관리합니다.(feature, hotfix)

- **feature:** develop 브랜치에서 신규 기능 개발을 위할 때 사용, feature/SOMETHING 의 명명으로 사용
- **hotfix:** 현재 출시된 버전에서 버그를 수정할 때 사용

다음 버전의 배포준비를 위해 release branch를 사용합니다(release)

- **release:** 다음 버전 배포 이전에 RC(Release Candidate)가 적용됩니다. (개발 서버는 해당 브렌치를 바라봅니다)
![Git-Flow](https://github.com/Lucky-pear/Git-guideline/blob/master/img/git-flow_overall_graph.png)


## Commit Guidelines

Commit message를 활용하여 배포 자동화 및 semantic versioning에 활용합니다

semantic-release를 활용하기 위해 Angular commit guideline을 따릅니다. 

### Types

- **feat:** 새로운 기능 추가
- **fix:** 버그 수정
- **docs:** 도큐멘테이션 변경
- **style:** 코드에 지장 없는 스타일 변경(공백, 세미콜론 추가, etc)
- **refactor:** 기능적으로나 버그를 수정한 리펙토링
- **perf:** 퍼포먼스 향상을 위한 코드 추가
- **test:** 테스트코드 추가
- **chore:** 빌드 프로세스 또는 도큐먼트 생성과 같은 툴 및 라이브러리 변경

### Example

#### 쇼핑(아이템 선택, 장바구니 담기 등) app을 개발한다고 가정,
- **feat:** 장바구니에 아이템 담기 기능 추가
- **fix:** 장바구니에 아이템이 안담기는 버그 수정
- **docs:** 프로젝트 readme.md 변경 등
- **style:** 코드에 세미콜론을 빼먹음, 연산자 사이에 공백 추가 등
- **refactor:** 장바구니 담기 코드가 비효율적이어서 효율적인 코드로 변경(내부적으로 변경, 외부적으론 차이가 없음)
- **perf:** 장바구니 담기는 속도가 너무 느려서 최적화 등
- **test:** 장바구니에 잘 담기는지에 대한 테스트 코드 작성
- **chore:** redux를 mobx로 교체 등

### Commit Guidelines
Commit 규칙을 설정해 commit graph를 관리합니다.

- 큰 주제의 기능은 feature/FEATURE로 브랜치를 생성 후 작업을 진행합니다.
- 작업을 시작하기 전에 Git issue를 생성합니다.
- Git issue를 연관된 project와 연결하고 내용에 맞는 라벨들을 기입합니다.
- 하나의 이슈는 되도록 하나의 커밋으로 합니다.
- 커밋 그래프는 최대한 단순하게 가져갑니다.
- 서로 공유하는 브랜치의 커밋 그래프는 함부로 변경하지 않습니다.
- 리뷰어에게 꼭 리뷰를 받습니다.(merge가 가능해도 진행하지 않습니다)


## References

[Git-Flow](https://woowabros.github.io/experience/2017/10/30/baemin-mobile-git-branch-strategy.html)
