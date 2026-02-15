## フローチャート

```mermaid
flowchart TD
A[開始] --> B[results を用意]
B --> C[calculate_total 呼び出し]

C --> D[total=0<br>first_count=0<br>i=0]

D --> E{i < len(data) ?}

E -- Yes --> F{data[i]==1 ?}
F -- Yes --> G[first_count+1]
F -- No --> H[そのまま]

G --> I[score_point加算]
H --> I

I --> J[totalに加算]
J --> K[i=i+1]
K --> E

E -- No --> L{first_count>=2 ?}

L -- Yes --> M[total+3]
L -- No --> N[そのまま]

M --> O[値を返す]
N --> O

O --> P[total表示]

P --> Q{total>=10<br>and<br>first_count>=1 ?}

Q -- Yes --> R[対象]
Q -- No --> S[対象外]

R --> T[終了]
S --> T
```
