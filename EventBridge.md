# EventBridge

## ルールの名前とステータスを取得

```
aws events list-rules | jq -r '.Rules | map({ Name: .Name, State: .State })'
```

```
[
  {
    "Name": "ecs-slack-notify",
    "State": "ENABLED"
  },
  {
    "Name": "start-ec2-instance",
    "State": "DISABLED"
  }
]
```
