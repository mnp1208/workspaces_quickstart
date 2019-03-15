1. Create users in Simple AD through web
2. Run CloudFormation
``` bash
aws cloudformation create-stack --stack-name WorkspacePOC --template-body file://workspaces.yaml --region us-east-1
```

aws workspaces describe-workspaces --region us-east-1
