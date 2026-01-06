# aws-mermaid

AWSアーキテクチャ図をmermaidで書いてみる
参考: <https://qiita.com/b-mente/items/89e900dab7319ef502be>

```mermaid
info
flowchart TB

subgraph ACCOUNT[AWS Account 123456789012]
  ELB@{ img: "https://api.iconify.design/logos/aws-elb.svg", label: "ELB", pos: "b", w: 60, h: 60, constraint: "on" }
  ECS@{ img: "https://api.iconify.design/logos/aws-ecs.svg", label: "ECS", pos: "b", w: 60, h: 60, constraint: "on" }
  RDS@{ img: "https://api.iconify.design/logos/aws-rds.svg", label: "RDS", pos: "b", w: 60, h: 60, constraint: "on" }
  CloudFront@{ img: "https://api.iconify.design/logos/aws-cloudfront.svg", label: "CloudFront", pos: "b", w: 60, h: 60, constraint: "on"}
    APIGateway@{ img: "https://api.iconify.design/logos/aws-api-gateway.svg", label: "APIGateway", pos: "b", w: 60, h: 60, constraint: "on"}
    Lambda@{ img: "https://api.iconify.design/logos/aws-lambda.svg", label: "Lambda", pos: "b", w: 60, h: 60, constraint: "on"}
  CloudFront --- ELB --- ECS --- RDS
  CloudFront --- APIGateway --- Lambda
end

classDef vpc fill:none,color:#0a0,stroke:#0a0
class ACCOUNT vpc
```
