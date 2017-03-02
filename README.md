# EkoJoiObjectId
Extending Joi to validate and convert mongo/mongoose ObjectId

## Installation

```
$ npm install eko-joi-objectid --save
```


## Usage Example

```
var Joi = require('joi');
var ObjectId = require('mongoose').Types.ObjectId;
Joi.objectId = require('eko-joi-objectid')(Joi, ObjectId);

var someObjectId = (new ObjectId()).toString();
var result = Joi.attempt(someObjectId, Joi.ObjectId());

result instanceof ObjectId; // => true
```