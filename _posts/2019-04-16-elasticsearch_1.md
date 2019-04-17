---
title: "Elstic Search 기본"
date: 2019-04-16 08:45:34 -0400
categories: Study
---

**ElasticSearch 기본 용어 정리**

Elasticsearch는 확장성이 뛰어난 오픈소스 풀텍스트 검색 및 분석 엔진입니다. 방대한 양의 데이터를 신속하게, 거의 실시간으로 저장, 검색, 분석할 수 있도록 지원합니다. 일반적으로 복잡한 검색 기능 및 요구 사항이 있는 애플리케이션을 위한 기본 엔진/기술로 사용됩니다

*Document*
 Elasticsearch 에 저장하는 기본 정보이다. 통상적 데이터베이스에서의 row라고 생각하면 된다. 
 document는 json객체로 저장되고 반드시 타입에 속해있어야 한다. 문서를 인덱스화 하는 기본 정보단위이다.

*Type*
Document의 공통적 field이다. 통상적 데이터베이스의 테이블로 생각하면 된다. 인덱스들을 논리적으로 분류하고 구분한것.  하지만 다소 

*Node* 
노드는 클러스터에 포함된 단일 서버. 데이터 저장과 클러스터의 indexing , 검색기능을 도운다. 노드는 클러스터처럼 이름으로 식별된다. Default 는 임의 uuid 이지만  원하는 이름으로 정의 할 수 있다.
다수의 노드가 같은 클러스터의 이름을 가짐으로써 하나의 클러스터에 속하도록 구성할 수 있다.

*Cluster*
하나이상의 노드가 모인것. 클러스터는 전체 데이터를 저장하고 모든 노드를 포괄하는 통합 indexing 및 검색기능을 제공한다.
고유이름으로 식별된다. 기본이름은 elastic search 이다.다수의 노드는 하나의 cluster 이름을 공유함으로 cluster 구성원이 될 수 있다. 동일한 cluster 이름은 서로다른 환경에서 사용하는 것은 위험하다.  ‘Log-dev’,’log-stage’ 등으로 구분하여 사용하는 것이 안전하다. 
