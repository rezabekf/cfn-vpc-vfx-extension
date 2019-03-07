# cfn-vpc-vfx-extension
Cloud formation template to deploy additional vpc for [quickstart-vfx-ise](https://github.com/aws-quickstart/quickstart-vfx-ise).

This is extension only and will not work without [quickstart-vfx-ise](https://github.com/aws-quickstart/quickstart-vfx-ise) framework deployed first.

####Prerequisites:
- Successfully deployed [quickstart-vfx-ise](https://github.com/aws-quickstart/quickstart-vfx-ise) framework.

- Make sure to deploy both Cloud Formation templates in a same AWS Region.

####Deployment:

- *Option 1:* via AWS console
> Go to https://console.aws.amazon.com/cloudformation/

> Double check that [quickstart-vfx-ise](https://github.com/aws-quickstart/quickstart-vfx-ise) is in Status CREATE COMPLETE.

> Upload the template file and fill in required Parameters.

> Create Stack 

- *Option 2:* using AWS Command Line
> from within the cfn-vpc-vfx-extension directory run command bellow 

`aws cloudformation create-stack --stack-name <MyStack> --template-body file://vpc-extension.template --parameters file://parameters.json --capabilities CAPABILITY_IAM --region <AWS-Region>`

> for example, if your quickstart-vfx-ise stack is deployed in Dublin region

`aws cloudformation create-stack --stack-name vpc-extension --template-body file://vpc-extension.template --parameters file://parameters.json --capabilities CAPABILITY_IAM --region eu-west-1`

