# BlockChainPOC

## [Directions GoogleDoc](https://docs.google.com/document/d/1jnLH4tmWWb6J4ankNvimDhy8bqHsFlJOO-LgZxo9kNs/edit?usp=sharing)


## Install Elastic Beanstalk command line tool
- [AWS Directions](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html)
- TLDR: ```python pip install awsebcli --upgrade --user ``` or *Recommended:* ```python pip3 install awsebcli --upgrade --user ```

```python eb terminate flask-env ```

## Deploy Flask Application to AWS
- [AWS Directions](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create-deploy-python-flask.html)
- Notes:
    1. After: ```python pip install flask==0.10.1 ``` *install requests* ```python pip3 install requests ``` or you can just copy the requirements.txt file from this repo!
    2. *Don’t use:* ```python ~/eb-flask$ eb init -p python2.7 flask-tutorial ``` Use: ```python eb init ``` and follow the prompts. 
    3. The remainder of the directions assume you name your environment ```python blockchain-env ```
    4. Python version is 3.6.0
    5. You can find the AWS credentials in the slack channel (look for an excel file) or you can create your own if you’re using your own Amazon account.
    6. You can open the Flask application using: ```python eb open ``` You should see a new tab open in your browser that looks like this:
    
    
    
    7. You can use the blockchain by executing *GET / POSTS* requests to the corresponding URL. For example given the base url returned from EB: “http://blockchain-env.frpxa3yuwp.us-east-1.elasticbeanstalk.com/” you can make requests to: 
        a. ‘/mine’
        b. ‘/transactions/new’
        c. ‘/chain’
        d. ‘/nodes/register’
        e. ‘/nodes/resolve’
        
   8. Sample EHR records are still executed on ‘/transactions/new’. JSON should be in the form: 
        
        ```javascript
{
          "patient": "Bart Simpson",
          "physician": "Doogie Howser",
          "date": "Feb 20, 2018",
          "notes": "Annual physical"
        }
```

   8. Be sure to *terminate* the instance when you’re done: ```python eb terminate blockchain-env ```
   
   



    
