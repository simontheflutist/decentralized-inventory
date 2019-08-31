# decentralized-inventory
This runs on AWS.
## install

    virtualenv venv/
    source venv/bin/activate
    pip3 install -r requirements.txt
    
    cd sam-app
    sam package --output-template /tmp/packaged.yml --s3-bucket simon-taug-sam
    sam deploy --template-file /tmp/packaged.yml --region us-east-1 --stack-name inventory
