```mermaid
graph LR
A[Load JSON File] --> B[Initialize Combined DataFrames]
B --> C{Iterate over JSON Files}
C --> D1{Iterate over Cases}
D1 -->|Cases Data| E1(Normalize Cases Data)
C --> D2{Iterate over Parties}
D2 -->|Parties Data| E2(Normalize Parties Data)
C --> D3{Iterate over Hearings}
D3 -->|Hearings Data| E3(Normalize Hearings Data)
C --> D4{Iterate over Documents}
D4 -->|Documents Data| E4(Normalize Documents Data)
E1 --> F[Append to Combined Cases DataFrame]
E2 --> F[Append to Combined Parties DataFrame]
E3 --> F[Append to Combined Hearings DataFrame]
E4 --> F[Append to Combined Documents DataFrame]
F --> G[Next JSON File]
G --> C


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
