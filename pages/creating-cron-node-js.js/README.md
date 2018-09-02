
# Create a Cron Job in Node.js

### Step 1 - Add node-cron to your project
Go to your project and run the following command:

```sh
npm install node-cron
``` 

### Step 2 - Import node-cron
In the file you are running the task from, import node-cron:

```javascript
var cron = require('node-cron')
```

### Step 3 - Usage
This step depends on how and when you want to run the task.<br/>
Read [this page](http://www.nncron.ru/help/EN/working/cron-format.htm) to see how to format a cron string. (Ommit the 6th * as it is not used in this module)<br/>
[This site](https://crontab.guru/#*_*_*_*_*) will help you format the cron string.
#### Run at Midnight Every Night

```javascript
cron.schedule('0 0 * * *', function(){
  //Run logic to see if the record is to be deleted. If it is, delete it.
});
```

#### Run Every Hour

```javascript
cron.schedule('0 * * * *', function(){
  //Run logic to see if the record is to be deleted. If it is, delete it.
});
```

#### Run Every 30 Minutes

```javascript
cron.schedule('30 * * * *', function(){
  //Run logic to see if the record is to be deleted. If it is, delete it.
});
```

#### Run Every Minute

```javascript
cron.schedule('* * * * *', function(){
  //Run logic to see if the record is to be deleted. If it is, delete it.
});
```

Created by [Cameron Ingham](https://github.com/Camji55)