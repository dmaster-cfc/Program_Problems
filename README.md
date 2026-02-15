flowchart TD
A[開始] --> B[結果を用意]
B --> C[calculate_total 呼び出し]

C --> D[合計=0<br>最初のカウント=0<br>i=0]

D --> E{i &lt; len(data)}
E -- はい --> F{data[i]==1}
E -- いいえ --> Eend[ループ終了]
Eend --> L{first_count &gt;= 2}

F -- はい --> G[最初の数+1]
F -- いいえ --> H[そのまま]
G --> I[score_point加算]
H --> I
I --> J[合計に加算]
J --> K[i=i+1]
K --> E

L -- はい --> M[合計+3]
L -- いいえ --> N[そのまま]
M --> O[値を返す]
N --> O

O --> P[合計表示]
P --> Q{合計 &gt;= 10 かつ first_count &gt;= 1}
Q -- はい --> R[対象]
Q -- いいえ --> S[対象外]
R --> T[終了]
S --> T

