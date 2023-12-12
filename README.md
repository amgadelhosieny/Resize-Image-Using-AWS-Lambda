# Resize-Image-Using-AWS-Lambda


# Step 1

create two s3 buckets first one to upload the image and second to show image after resize

# step 2

create IAM policy to give the permissions to lambda so it can access s3 bucket and see any change happens

# step 3

make Execution Role to connect IAM Policy to lambda function

# step 4

write the following commands:

command 1)

mkdir package

Command 2) install the Pillow (PIL) library and dependencies

sudo apt update \
pip3 install \
--platform manylinux2014_x86_64 \
--target=package \
--implementation cp \
--python-version 3.9 \
--only-binary=:all: --upgrade \
pillow boto3

Command 3) go to package folder

cd package

Command 4) Zip the contents of the package folder

zip -r ../lambda_function.zip .

Command 5) Go back to the project folder

cd ..

Command 6) Zip the lambda_function.py file into the lambda_function.zip file

zip lambda_function.zip lambda_function.py


# step 5

create lambda fuction and upload your python code in it

# step 6

make an trigger to lambda so it can take actions whenever images uploaded to s3
