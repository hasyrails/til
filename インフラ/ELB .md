## ELB (Elastic Load Balancing)

### ELBによる冗長化構成の構築
ELBの冗長化は負荷分散

### ELBの種類
・Application Load Balancer  
・Network Load Balancer  
・Classic Load Balancer (レガシー)  
  
基本的にはApplication Load Balancer  

[PC] ←（HTTPレスポンス）→　[ELB]　←（HTTPレスポンス）→ [EC2]

### ELB自体の負荷分散は不要
ELB自体の負荷分散のためにELBを複数用意する必要はない  
Amazonに任せる  
