# 건물 기본 정보

- 100개의 building_number
- 12가지 building_type

>Other_Buildings       15\
>Public          8\
>University         8\
>Department_Store_and_Outlet     8\
>Hospital          8\
>Commercial          8\
>Apartment         8\
>Research_Institute         8\
>Knowledge_Industry_Center      8\
>Discount_Mart        8\
>Hotel_and_Resort      8\
>Data_Center       5

- 태양광용량(kW)(solar_power_capacity) : 태양광 발전 설비가 설치된 건물 36개소
> 태양광을 사용하여 전력을 생산할 수 있는 능력


- ESS 시스템 : ESS 시스템 베터리 + PCS(Power Conversion System)이 설치된 건물 5개소
    - ESS 저장용량(kWh): (ESS 시스템 베터리 용량)
>생산된 전기에너지를 저장하여 전력 이 필요한 시기에 사용할 수 있게 하는 에너지 솔루션
>  - PCS(Power Conversion System): ESS 내 전력변환장치 
>PCS는 저장된 에너지를 효율적으로 변환하고 제어하는 역할\
>PCS의 용량은 ESS에서 저장된 에너지를 공급할 수 있는 능력을 나타낸다

\* 태양광 발전 설비와 ESS 시스템이 모두 설치된 건물: 2개소

# 1. 태양광 발전설비 설치 비율
- 대학교, 연구소, 병원 순으로 태양광 발전설비 설치율이 높음
- 아파트, 지식산업센터, 데이터센터에는 태양광 발전설비를 설치하지 않음

# 2. 상관관계 분석
- 정도가 크지 않았지만 `power_consumption`와 `solar_radiation`, `temperature`,`WCT` 순으로 높은 상관관계를 보임

# 3. 시간당 최대, 최소 전력사용량
- 100개의 빌딩에 전원을 정상적으로 공급하기 위해서는 최소 368310.21(kWh)이상의 전기를 공급할 수 있는 설비가 필요함
> 2022-08-05(금) 13:00:00에 기간내 시간당 최대 전력사용량으로 368310.21(kWh)을 기록\
>  2022-06-07(화) 03:00:00에 기간내 시간당 최소 전력사용량으로 148285.615(kWh)을 기록

# 4. 요일별 전력사용량 평균
- 화요일에 전력사용량 평균이 가장 높음

# 5. 건물별_요일별_전력사용량_평균
- '건물기타': 'Other_Buildings',
- '공공': 'Public' - 주말 전력 소비 감소
- '대학교': 'University' - 주말 전력 소비 감소
- '데이터센터': 'Data_Center' - 매일 전력 소비 일정
- '백화점및아울렛': 'Department_Store_and_Outlet' - 월요일 전력 소비 감소
- '병원': 'Hospital' - 주말 전력 소비 감소
- '상용': 'Commercial' - 주말 전력 소비 감소
- '아파트': 'Apartment' - 매일 전력 소비 일정
- '연구소': 'Research_Institute' - 주말 전력 소비 감소
- '지식산업센터': 'Knowledge_Industry_Center' - 주말 전력 소비 감소
- '할인마트': 'Discount_Mart' - 일요일 전력 소비 감소
- '호텔및리조트': 'Hotel_and_Resort' - 매일 전력 소비 일정

# 6. 월별 건물별 전력소비량 평균
- 2022년 8월 27번 건물이 월평균 전력소비량 평균이 가장 높음
- 2022년 8월 66번 건물이 월평균 전력소비량 평균이 가장 낮음

# 7. 월별 건물별 단위 면적당 전력소비량
- 13번 건물의 단위 면적당 전력소비량이 가장 높음
- 20번 건물의 단위 면적당 전력소비량이 가장 낮음

# 8. 건물별 시간당 전력소비량 빈도
- 사례의 100개 건물의 시간당 전력 사용량 약 98%는 10000kWh 이하
> 일반적으로 한 건물에서 전력을 공급하기 위한 전력 공급 설비 용량은 10000kWh 수준으로 준비

- 건물의 시간당 최대 전력소비량은 2022-07-06 15:00:00 27번 건물에서 발생한 25488.4kWh
> 특수한 경우를 대비하여 25488.4kWh 이상의 전력 공급 설비도 대비가 필요
