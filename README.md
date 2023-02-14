
# Welcome to your CDK Python project!

You should explore the contents of this project. It demonstrates a CDK app with an instance of a stack (`aws_cdk_workshop_stack`)
which contains an Amazon SQS queue that is subscribed to an Amazon SNS topic.

The `cdk.json` file tells the CDK Toolkit how to execute your app.

This project is set up like a standard Python project.  The initialization process also creates
a virtualenv within this project, stored under the .venv directory.  To create the virtualenv
it assumes that there is a `python3` executable in your path with access to the `venv` package.
If for any reason the automatic creation of the virtualenv fails, you can create the virtualenv
manually once the init process completes.

To manually create a virtualenv on MacOS and Linux:

```
$ python3 -m venv .venv
```

After the init process completes and the virtualenv is created, you can use the following
step to activate your virtualenv.

```
$ source .venv/bin/activate
```

If you are a Windows platform, you would activate the virtualenv like this:

```
% .venv\Scripts\activate.bat
```

Once the virtualenv is activated, you can install the required dependencies.

```
$ pip install -r requirements.txt
```

At this point you can now synthesize the CloudFormation template for this code.

```
$ cdk synth
```

You can now begin exploring the source code, contained in the hello directory.
There is also a very trivial test included that can be run like this:

```
$ pytest
```

To add additional dependencies, for example other CDK libraries, just add to
your requirements.txt file and rerun the `pip install -r requirements.txt`
command.

## Useful commands

 * `cdk ls`          list all stacks in the app
 * `cdk synth`       emits the synthesized CloudFormation template
 * `cdk deploy`      deploy this stack to your default AWS account/region
 * `cdk diff`        compare deployed stack with current state
 * `cdk docs`        open CDK documentation

Enjoy!

## Next Steps

### Preliminary preparations
* `source .venv/bin/activate` 
* `python3 -m pip install --upgrade pip` 
* `pip install -r requirements.txt`
* `brew upgrade awscli` para MacOS 
* `aws --version` 
* `brew upgrade aws-cdk` para MacOS
* `cdk --version`

### Synthesize a template from your app
* `cdk ls` 
* `cdk synth` 

### Bootstrapping an environment
Install the bootstrap stack into an environment:
- `cdk bootstrap --profile profile_name` with the use of [AWS IAM Identity Center](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-sso.html) (previous configuration)
- Create stack on the Cloudformation of the account in the profile: This stack includes resources needed to deploy AWS CDK apps into this environment
- We can use the AWS CloudFormation console in order to manage the stacks.

### Let’s deploy
- Use `cdk deploy --profile profile_name` to deploy a CDK app
- On AWS Cloudformation Console is **cdk-workshop** we can open the **Resources tab**, we will see the physical identities of our resources.

## Acknowledgements
- [The Python CDK Workshop](https://cdkworkshop.com/30-python.html)
- [Automatic authentication refresh for AWS IAM Identity](https://docs.aws.amazon.com/cli/latest/userguide/sso-configure-profile-token.html)
