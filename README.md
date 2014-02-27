Simulations and Artificial Behaviours
=====================================

Workshop at [CIID](http://ciid.dk), Copenhagen, February 2014 by [David Gauthier](http://gauthiier.info) & [Marcin Ignac](http://marcinignac.com)


## Day 4: Signals

Include signals library

	<script type="text/javascript" src="js/signals-data.js"></script>
	<script type="text/javascript" src="js/signals.js"></script>

### Bitcoin
	
**Properties:**

`value` - bitcoin price level (0..1)  
`avgValue` - avg bitcoin price level (0..1)  
`delta` - bitcoin price level change (-1..1)  
`price` - bitcoin price in US dollars

**Events:**

*None*


**Example:**

	var bitcoin = new BitcoinSignal();
		
	function onFrame(event) {
		bitcoin.update(event.time)
		console.log(bitcoin.value);
		console.log(bitcoin.avgTime);
		console.log(bitcoin.delta);
		console.log(bitcoin.price);
	}
	
### Email
	
**Properties:**

`value` - new email level (0..1)  
`avgValue` - avg new email level (0..1)  
`delta` - new email level change (-1..1)  
`count` - number of new emails

**Events:**

`onEmail` - fired when new email arrives


**Example:**

	var email = new EmailSignal();
		
	function onFrame(event) {
		email.update(event.time)
		console.log(email.value);
		console.log(email.avgTime);
		console.log(email.delta);
		console.log(email.count);
		glucose.onEmail = function(count) {
			console.log('You've got a message!')
		}
	}

### Glucose
	
Properties:

`value` - glucose level (0..1)  
`avgValue` - avg glucose level (0..1)   
`delta` - glucose level change (-1..1)    
`level` - glucose level (raw data)  
`carbs` - carbohydrates level (food) (raw data)

Events:

`onFood` - fired when patient eats food

Example:


	var glucose = new GlucoseSignal();
	
	function onFrame(event) {
		glucose.update(event.time)
		console.log(glucose.value);
		console.log(glucose.avgTime);
		console.log(glucose.delta);
		console.log(glucose.level);
		glucose.onFood = function(carbs) {
			console.log('mniam mniam!')
		}
	}

### Weather

Properties:

`value` - wind speed level (0..1)  
`avgValue` - avg wind speed level (0..1)   
`delta` - wind speed level change (-1..1)    
`windSpeed` - wind speed  
`windDirection` - wind direction  
`temperature` - temperature  

Events:

*none*

Example:


	var weather = new GlucoseSignal();
	
	function onFrame(event) {
		weather.update(event.time)
		console.log(weather.value);
		console.log(weather.avgTime);
		console.log(weather.delta);
		console.log(weather.windSpeed);
		console.log(weather.windDirection);
		console.log(weather.temperature);
	}


