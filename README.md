# connect-to-aws
example on how to connect python to aws &amp; manage instance

This is a project thats shows how to use boto3 to manage AWS instances from python

Created a user called apiuser1 in aws account to test access of aws thru python
used aws configure to configure that user to aws cli

aws configure --profile awsapi1  # this name shld have been apiuser1

connect-to-aws is the project created in github
c:\rajesh\githubcode\connect-to-aws

cd c:\rajesh\githubcode\connect-to-aws
pip3 install pipenv (install pipenv in the project directory)

pipenv --three

pipenv install boto3
pipenv install -d ipython


pipenv run ipython
import boto3
session = boto3.Session(profile_name='awsapi1')
ec2 = session.resource('ec2')

for i in ec2.instances.all():
	print(i)
	
use pipenv to run a python file
pipenv run python shotty/shotty.py

or
python shotty/shotty.py



