# pypi-awssnippets
Python3 classes and functions to execute common AWS operations.

## Usage Example

```python
"""Read secret string from AWS Secrets Manager."""
import aws_snippets

# secret_string = aws_snippets.readsecret('<secret-ID>')
secret_string = aws_snippets.readsecret('dkfjh765-sdfsf456-dfgd')
print(secret_string)

# Output: "I'm Batman!"
```

## Get Full Functionality List from Docstring

### Python Commands

```python
import aws_snippets
help(aws_snippets)
```

### BASH Commands

```bash
python -c 'import aws_snippets; help(aws_snippets)'
```

### Output

```txt
Help on package aws_snippets:

NAME
    aws_snippets - Execute AWS operations.

PACKAGE CONTENTS


CLASSES
    builtins.object
        WriteLog
    
    class WriteLog(builtins.object)
     |  WriteLog(text)
     |  
     |  Create JSON log object for CloudWatch.
     |  
     |  # Import modules.
     |  import json
     |  from aws_snippets import WriteLog
     |  
     |  # Initiate with empty dictionary.
     |  logger = WriteLog({})
     |  
     |  # Collect entries to log.
     |  logger.log('<strkey>', '<value>')
     |  logger.log('<intkey>', <value>)
     |  logger.log('<boolkey>', <True/False>)
     |  
     |  # Print out to CloudWatch as accumulated log.
     |  print(json.dumps(logger.text))
     |  
     |  Methods defined here:
     |  
     |  __init__(self, text)
     |      Initialize log content.
     |  
     |  log(self, key, value)
     |      Update log content.
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)

FUNCTIONS
    b64encode(cleartext: str, encoding: str = 'latin-1') -> str
        Encode strings using Base64.
        
        return str
    
    cfpurge(cf_dist: str, path: str, call_ref: str) -> dict
        Create Amazon CloudFront cache invalidation.
        
        return dict
    
    cleantmp(tmppath: str) -> None
        Clean Lambda /tmp path.
        
        return None
    
    dynamodbcreatetable(table: str, attrdictls: list, schemadictls: list, kmsid: str, tagdictls: list) -> None
        Create a table in DynamoDB.
        
        return None
    
    dynamodbdeleteallitems(table: str) -> None
        Delete all items from a DynamoDB table.
        
        return None
    
    dynamodbdeletetable(table: str) -> None
        Delete a table from DynamoDB.
        
        return None
    
    dynamodbgetitem(table: str, key: str, value: str) -> dict
        Get a single item from DynamoDB.
        
        return dict
    
    dynamodbputitem(table: str, itemdict: dict) -> None
        Put a single item into DynamoDB.
        
        return None
    
    dynamodbqueryitems(table: str, key: str, value: str) -> dict
        Get items based on keyword query from DynamoDB.
        
        return dict
    
    dynamodbscanallitems(table: str) -> dict
        Get all items from a table in DynamoDB.
        
        return dict
    
    dynamodbscanitems(table: str, key: str, value: str, patternexp: dict) -> dict
        Get all items from a DynamoDB table then filter by expression.
        
        return dict
    
    dynamodbupdateitem(table: str, keydict: dict, attributedict: dict, valuedict: dict, updateexpression: str) -> dict
        Update an item in a DynamoDB table.
        
        return dict
    
    httpget(url: str, headers: dict = {}, encoding: str = 'latin-1') -> dict
        Make HTTP requests using GET method.
        
        return dict
    
    httppost(url: str, headers: dict = {}, data: dict = {}, encoding: str = 'latin-1') -> str
        Make HTTP requests using POST method.
        
        return str
    
    kmsdecrypt(ciphertext: str, kmsid: str) -> str
        Decrypt strings using AWS KMS.
        
        return str
    
    kmsencrypt(cleartext: str, kmsid: str) -> str
        Encrypt strings using AWS KMS.
        
        return str
    
    randomize(length: int, punctuations: bool = False) -> str
        Create random strings.
        
        return str
    
    readsecret(id: str) -> str
        Read secret values in AWS Secrets Manager.
        
        return str
    
    sanitizerclean(input: str) -> str
        Sanitize input items.
        
        return str
    
    sanitizercleanlist(input: list, pattern: str) -> list
        Sanitize input list.
        
        return list
    
    sanitizercleanurl(url: str) -> str
        Sanitize input URLs.
        
        return str
    
    sanitizercleanurllist(input: list, pattern: str) -> list
        Sanitize input list.
        
        return list
    
    sanitizervalidate(input: str, pattern: str) -> bool
        Validate input items to RegEx patterns.
        
        return bool
    
    sanitizervalidatelist(input: list) -> bool
        Validate input list.
        
        return bool
    
    sha3512hash(clrtxt: str, condiments: str, encoding: str = 'latin-1') -> str
        Hash strings using SHA3_512 algorithm.
        
        return str
    
    snsnotify(topic: str, message: str, subject: str) -> None
        Send AWS SNS notifications.
        
        return None
    
    sqsmessage(queue_url: str, message: dict) -> dict
        Send messages into AWS SQS queues.
        
        return dict

DATA
    Union = typing.Union
        Union type; Union[X, Y] means either X or Y.
        
        To define a union, use e.g. Union[int, str].  Details:
        - The arguments must be types and there must be at least one.
        - None as an argument is a special case and is replaced by
          type(None).
        - Unions of unions are flattened, e.g.::
        
            Union[Union[int, str], float] == Union[int, str, float]
        
        - Unions of a single argument vanish, e.g.::
        
            Union[int] == int  # The constructor actually returns int
        
        - Redundant arguments are skipped, e.g.::
        
            Union[int, str, int] == Union[int, str]
        
        - When comparing unions, the argument order is ignored, e.g.::
        
            Union[int, str] == Union[str, int]
        
        - You cannot subclass or instantiate a union.
        - You can use Optional[X] as a shorthand for Union[X, None].

VERSION
    2021.1.0.0

FILE
    /Users/abdahmad/Desktop/aws_snippets/__init__.py
```
