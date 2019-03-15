
1. Create the networking required:
  ``` bash
  aws cloudformation create-stack \
    --stack-name WorkspacePocNetworking \
    --template-body file://networking.yaml \
    --parameters file://networking-parameters.json \
    --region us-east-1
  ```
2. Create the end user computing required:
  ``` bash
  aws cloudformation create-stack \
    --stack-name WorkspacePocEndUserComputing \
    --template-body file://end-user-computing.yaml \
    --parameters file://end-user-computing-parameters.json \
    --region us-east-1
  ```
3. Create the compute instance(s) required:
  ``` bash
  aws cloudformation create-stack \
    --stack-name WorkspacePocCompute \
    --template-body file://compute.yaml \
    --parameters file://compute-parameters.json \
    --region us-east-1
  ```

  
aws workspaces describe-workspaces --region us-east-1
