---
title: "비용 분석"
linkTitle: "비용 분석"
weight: 3
date: 2022-06-23
description: >
    **비용 분석**은 클라우드 제공자로부터 수신되는 비용 데이터를 상세하게 분석합니다.
    <br>
    <br>
    다양한 조건으로 데이터를 그룹화 혹은 필터링하여, 원하는 비용 데이터를 한눈에 볼 수 있습니다.
---

## 비용 분석 확인하기

### 세부기준 선택하기

**세부 기준**은 데이터를 어떤 방식으로 보여줄 것인가에 대한 기준입니다. 세부 기준에 따라 제공되는 차트나 테이블의 형태가 달라집니다.

{세부기준 선택 이미지}

- `누적 데이터`: 파이차트가 제공되며, 테이블에서는 선택한 기간의 데이터 총합을 보여줍니다.
  - {이미지}
- `일별 데이터` 혹은 `월별 데이터`: 칼럼차트가 제공되며, 테이블에서는 선택한 기간을 일별, 월별로 보여줍니다.
  - {이미지}

### 기간 설정하기
세부 기준에 따라 선택할 수 있는 기간 메뉴가 다르게 나타납니다. [기간] 드롭다운에서 메뉴를 선택하거나, [기간 선택] 메뉴를 통해 직접 설정합니다.

{이미지}

`누적 데이터`와 `월별 데이터`는 월 단위로 커스텀 가능하며 기간은 최대 12개월까지 지정할 수 있습니다.
`일별 데이터`의 경우 일 단위로 커스텀 가능하며 기간은 최대 1개월입니다.

{이미지}

### 환율 설정하기
[환율] 드롭다운에서 적용하려는 환율을 선택하면, 차트와 테이블의 비용 데이터에 환율이 적용됩니다.

{이미지}

### 그룹별 통계 설정하기
그룹별 통계에서 유저가 선택한 값을 기준으로 데이터를 그룹화합니다.

{이미지}

그룹별 통계는 한 개 이상 선택할 수 있습니다. 차트에서는 선택한 그룹별 통계 중 하나만이 보여지며, 테이블에서는 선택한 그룹별 통계를 모두 볼 수 있습니다.

{이미지 2개}

### 필터 설정
필터는 그룹별 통계와 마찬가지로 한 개 이상 선택 가능하며, 유저가 설정한 값을 and 조건으로 필터링합니다.

(1) [필터 추가] 아이콘 버튼을 클릭합니다.

{이미지}

(2) [필터 세팅] 모달이 열리면 원하는 필터를 선택한 뒤 [확인] 버튼을 클릭합니다.

{이미지}


## 비용 분석 쿼리
[비용 관리 > 비용 분석] 페이지에 진입할 때마다 세부 기준과 기간 등을 다시 설정해야 하는 번거로움을 해소하기 위해, 자주 사용하는 설정들을 쿼리로 저장할 수 있는 기능이 제공됩니다.
{{<alert>}}
환율은 쿼리에 저장되지 않습니다.
{{</alert>}}

### 쿼리 저장하기
(1) 세부 기준과 그룹별 통계, 필터 등을 설정합니다.

(2) 우측 상단의 [다른 이름으로 저장] 버튼을 클릭합니다.

{이미지}

{{<alert>}}
default 쿼리의 경우 [다른 이름으로 저장] 버튼이 나타나며, 기존 쿼리를 수정했을 경우 [저장] 버튼과 [다른 이름으로 저장] 버튼이 함께 나타납니다.
{{</alert>}}

(3) [쿼리 저장] 모달에서 쿼리명을 입력한 뒤, [확인] 버튼을 클릭합니다.

{이미지}

### 쿼리 불러오기
[비용 분석] 페이지에서 좌측 상단의 [쿼리 목록] 아이콘 버튼을 클릭한 뒤, 저장된 쿼리 목록 중 하나를 선택해 해당 쿼리를 불러올 수 있습니다.

{이미지}

### 쿼리 이름 편집하기
저장된 쿼리의 이름은 [비용 분석] 페이지에서 해당 쿼리를 불러온 뒤 [편집] 버튼을 클릭하거나, 저장된 쿼리 목록에서 [편집] 버튼을 클릭하여 편집할 수 있습니다.

{이미지 2개}

### 쿼리 삭제하기
저장된 쿼리는 [비용 분석] 페이지에서 해당 쿼리를 불러온 뒤 [삭제] 버튼을 클릭하거나, 저장된 쿼리 목록에서 [삭제] 버튼을 클릭하여 삭제할 수 있습니다.

{이미지 2개}