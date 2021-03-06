### Install Packages for Layers

```
pip3 install -r requirements.txt -t ./layers/python/
```

```
python3 -m pip install -r requirements.txt -t ./layers/python/
```

### Package & Deploy Program Stack

```
sam package --template-file ./stacks/sam-program-template.yaml --s3-bucket st-lambda-artifacts --output-template-file ./stacks/sam-program-output-template.yaml

sam deploy --template-file ./stacks/sam-program-output-template.yaml --stack-name safe-program-metrics --capabilities CAPABILITY_IAM
```

### Delete a Stack

```
aws cloudformation delete-stack --stack-name [stack-name]

aws cloudformation delete-stack --stack-name safe-program-metrics
```
