# aws-mermaid

AWSアーキテクチャ図をmermaidで書いてみる  
参考: <https://qiita.com/b-mente/items/89e900dab7319ef502be>

```mermaid
info
```

```mermaid
flowchart TB

subgraph ACCOUNT[AWS Account]
  subgraph GRP1[" "]
    ELB@{ img: "https://api.iconify.design/logos/aws-elb.svg", label: "ELB", pos: "b", w: 60, h: 60, constraint: "on" }
  end
  subgraph GRP2[" "]
    EC2@{ img: "https://api.iconify.design/logos/aws-ec2.svg", label: "EC2", pos: "b", w: 60, h: 60, constraint: "on" }
  end
  subgraph GRP3[" "]
    RDS@{ img: "https://api.iconify.design/logos/aws-rds.svg", label: "RDS", pos: "b", w: 60, h: 60, constraint: "on" }
  end
  ELB --- EC2 --- RDS
end

classDef vpc fill:none,color:#0a0,stroke:#0a0
class ACCOUNT vpc

classDef group fill:none,stroke:none
class GRP1,GRP2,GRP3 group
```
