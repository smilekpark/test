# test

```mermaid

graph TD
A[계획 수립]
B[하드웨어 준비]
C[소프트웨어 개발]
D[테스트 및 최적화]
E[모니터링 및 유지 보수]

A -->|1. 목표 설정<br>2. 예산 설정| B
B -->|1. 성장실 설계<br>2. 센서 선택<br>3. 제어 시스템 선택<br>4. 박막 수경재배 시스템 설치| C
C -->|1. 라이브러리 설치<br>2. 센서 인터페이스<br>3. 제어 로직 개발<br>4. 데이터 로깅| D
D -->|1. 시스템 테스트<br>2. 최적화| E
E -->|1. 모니터링<br>2. 유지보수| E

style A fill:#ffcccc,stroke:#333,stroke-width:2px
style B fill:#ccffcc,stroke:#333,stroke-width:2px
style C fill:#ccccff,stroke:#333,stroke-width:2px
style D fill:#ffffcc,stroke:#333,stroke-width:2px
style E fill:#ffccff,stroke:#333,stroke-width:2px
