# **1. 프로젝트 소개**

## **1-1. 프로젝트 개요**

본 프로젝트는 **Arduino Nano 33 BLE** 보드의 **자이로 센서**를 활용하여 운동 중 속도 변화를 감지하고, 급격한 변화 발생 시 경고음을 출력하는 운동 보조 시스템을 개발하는 것을 목표로 합니다.

## **1-2. 프로젝트 목표**

이 프로젝트는 운동 중 발생하는 **속도 변화 데이터를 실시간으로 분석**하고, 사용자가 힘이 빠지거나 급격한 속도 저하가 감지될 경우 **경고음을 출력**하여 부상을 예방하는 것을 목적으로 합니다. 이를 위해,

- **논문 기반 평균 운동 속도를 활용하여 데이터를 정규화**하고,
- **Sigmoid 함수를 활용하여 임계값을 설정**하여 경고음을 발생시키는 시스템을 구현합니다.

## **1-3. 프로젝트 주요 내용**

1. **운동 중 Z축 각속도 데이터 수집**
    - 벤치 프레스, 밀리터리 프레스, 데드리프트, 스쿼트 등의 운동을 대상으로 함
    - 운동 속도를 샘플링하여 실시간으로 분석
2. **논문 기반 평균 운동 속도 확보 및 데이터 정규화**
    - 기존 연구에서 발췌한 평균 운동 속도를 기준값(Reference Speed)으로 설정
    - 수집된 속도를 기준값과 비교하여 정규화 수행
3. **Sigmoid 함수를 활용한 속도 변화 감지 및 경고음 출력**
    - 정규화된 속도를 Sigmoid 함수에 입력하여 확률값 계산
    - 설정된 임계값 이하일 경우 경고음 발생
4. **경고음 발생을 통한 부상 방지**
    - BLE 통신을 활용하여 경고음을 출력하는 기능 추가
5. **향후 발전 가능성**
    - 경고음 대신 무게 조절 기능 추가
    - 운동 자세 교정 및 실시간 피드백 기능 추가

# **2. 파일 구성 및 활동 내용**

주 활동 내용은 다음과 같으며, 각 활동에 대한 자세한 내용은 각가의 폴더에 있는 README.md 파일을 참고한다.

1. Arduino Nano 33 BLE 보드 선정 이유 및 기능 소개
2. 데이터 처리 프로세스 설계
   1. 데이터 수집 처리 과정 처리
   2. 원시데이터의 노이즈 제거 및 필터링 작업
   3. 데이터의 정규화 및 표준화 과정
3. CNN 및 Transformer 기반 모델 설계
4. 샘플 데이터 수집
5. 샘플 데이터 분석 및 CNN 모델 생성
6. 실제 데이터 수집
7. 실제 데이터 분석 및 CNN 모델 생성
8. 임베디드 보드 구성
9. 통합 테스트 및 최종 검증
