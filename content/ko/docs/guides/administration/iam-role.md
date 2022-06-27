---
title: "[IAM] 역할"
linkTitle: "[IAM] 역할"
weight: 2
date: 2022-06-07
description: >
    역할은 권한에 대한 범위를 정의한 단위입니다.
---

관리자가 원하는 역할을 생성하여 해당 역할을 수행할 [사용자](/ko/docs/guides/administration/iam-user/)들에게 할당할 수 있습니다.

역할에 설정되는 속성들은 아래와 같습니다.

#### 역할(Role) 타입

|  | 프로젝트 관리 권한 | 역할을 사용자에게 부여하는 위치 |
| --- | --- | --- |
| **User** | • 사용자 직접 생성 <br/>• 초대받은 프로젝트와 프로젝트 그룹<br/>• 권한이 있는 프로젝트 그룹의 하위 프로젝트 | • 프로젝트 상세 페이지 > [멤버] 탭에서 프로젝트에 사용자를 초대<br/>• 멤버의 정보를 변경하는 경우 User 타입의 역할을 변경 가능 |
| **Admin** | 모든 프로젝트와 프로젝트 그룹 | [관리 > 사용자 및 권한 관리 > 사용자] 페이지에서 사용자를 추가 또는 편집 시 가능 |

#### 클라우드포레 서비스의 페이지별 접근 권한

각 서비스 세부 메뉴별로 `View`와 `Manage` 권한을 다르게 부여할 수 있습니다.

- **View**

  각 페이지들에 대하여 보기 권한이 주어집니다.

- **Manage**

  선택한 서비스 메뉴에 존재하는 생성, 편집, 추가 등과 같은 관리기능을 사용할 수 있습니다. (각 서비스/페이지 별로 관리기능은 상이합니다.)


#### API 정책 연결

정책(Policy)은 리소스에 연결될 때 해당 권한을 정의하는 개체입니다.

정책에대한 안내는 [정책 문서](/ko/docs/guides/administration/iam-policy)를 참고하십시오.

계속해서 역할에 대해 생성 / 편집 / 삭제 방법을 알아보겠습니다.

## 역할 생성하기

{{< alert title="" >}}
역할은 관리자만 생성할 수 있습니다. [생성] 버튼이 활성화 되어있지 않다면 관리자에게 권한을 요청하세요.
{{< /alert >}}




(1) [관리 > 사용자 및 권한 관리 > 역할] 메뉴를 선택해 역할 페이지에 진입합니다.

(2) 좌측상단 [생성] 버튼을 통해서 [역할 생성] 페이지에 진입합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/12c8d015-1b5b-4a94-9bea-23dd1be567d7/Untitled.png)

(3) 역할의 이름, 설명(선택)을 작성하고, [역할 타입](/ko/docs/guides/administration/iam-role/#역할role-타입)을 선택해 줍니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/38e7feaa-19a4-4b50-bcc3-453ae24d47bc/Untitled.png)

- [이름]은 최소 2글자 이상으로 작성되어야 합니다.
- [[역할 타입]](/ko/docs/guides/administration/iam-role/#역할role-타입)은 생성 이후 수정이 불가능한 항목이므로, 신중하게 선택해주세요.

(4) [페이지 접근권한](/ko/docs/guides/administration/iam-role/#클라우드포레-서비스의-페이지별-접근-권한)에 대해 설정해 줍니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f80ed10b-221c-423b-9220-e5bd782ec722/Untitled.png)

(5) 생성하려는 역할(Role)에 어떤 권한을 부여할지를 결정하기 위해, 정책(Policy)을 선택하여 연결합니다.

![스크린샷 2022-06-02 오전 11.32.27.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/75615cae-def8-4fa7-bf91-a67e866fb631/스크린샷_2022-06-02_오전_11.32.27.png)

정책(Policy)관련 자세한 설명은 여기를 참고해 주십시오.

(6) [생성] 버튼을 클릭하여 역할 생성을 완료합니다.

## 역할 조회하기

생성된 역할들은 조회, 검색 그리고 상세 정보 확인이 가능합니다.

### 역할 목록 조회하기

생성이 완료된 역할들은 역할 페이지에서 조회할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d0b5c6b2-310b-4d4a-a1e7-5ab04f6bb1ba/Untitled.png)

검색어를 입력하여 조건에 부합하는 역할 목록을 확인할 수 있습니다. 고급 검색에 대한 상세 설명은 [여기](/ko/docs/guides/advanced/search/)를 참고하세요.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bac43317-eef0-4bc1-959d-16215437d3b8/Untitled.png)

### 역할 상세 정보 확인하기

목차에서 역할 선택 시, 아래 [상세 정보] 탭에서 선택된 역할의 정보를 확인할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4491ee0e-3d44-4661-9c36-5f2af86afd1e/Untitled.png)

## 역할 편집하기

### Steps

(1) 편집하고자 하는 역할을 역할 목록에서 선택하고, [편집] 버튼을 클릭하여 편집 페이지에 진입합니다.

![스크린샷 2022-06-02 오전 10.47.08.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/61fa51f9-780c-43b7-b5a3-8c56a5bf85c4/스크린샷_2022-06-02_오전_10.47.08.png)

(2) 역할 타입 이외에 수정사항은 [역할 생성하기](/ko/docs/guides/administration/iam-role/#역할-생성하기)와 동일합니다.

![스크린샷 2022-06-03 오전 10.04.12.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/feb2bd9c-506e-4573-9ff2-db10ebc79ab0/스크린샷_2022-06-03_오전_10.04.12.png)

기본정보의 [역할 타입]은 생성이후 수정이 불가능한 항목입니다.

## 역할 삭제하기

### Steps

(1) 삭제하고자 하는 역할 페이지에 진입합니다.

![스크린샷 2022-06-02 오전 10.55.02.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/45b8e78e-c6d3-46ea-a079-ceec5b64d113/스크린샷_2022-06-02_오전_10.55.02.png)

삭제 시에 여러 역할을 한 번에 제거할 수 있습니다.

(2) [확인] 버튼을 클릭하여 삭제를 완료합니다.

이전 삭제 목록에서 선택한 역할들을 확인할 수 있습니다.

![스크린샷 2022-06-02 오전 10.59.54.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7b29b64d-f64a-4d60-a236-4b1586be4744/스크린샷_2022-06-02_오전_10.59.54.png)

{{< alert title="주의" >}}
삭제 대상인 역할이 부여되어있는 사용자가 존재하면 삭제할 수 없습니다.

![스크린샷 2022-06-02 오전 11.00.27.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a7d6b15e-4f45-4c6c-89d3-6b944cc95396/스크린샷_2022-06-02_오전_11.00.27.png)

삭제가 불가능한 역할이 포함되어있는 경우, 역할과 해당 역할이 할당된 사용자를 함께 보여줍니다.
{{< /alert >}}