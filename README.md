## express-cache-router

Router cache middleware for express. Useful for caching some pages like `/home`.

### Install

```
npm i express-cache-router --save
```

### Usage

```
var router = require('express').Router();
var CacheMiddleware = require('express-cache-router');
router.use('/home', CacheMiddleware({
    expire:5*60*1000
}));

router.get('/home', function*(){
    res.end('body');
});
```

Options :

- expire: expire time, use `ms`. (Required)

### License

MIT
