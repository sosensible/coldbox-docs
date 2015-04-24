# Interceptors

All interceptor events receive the following arguments:

* event - The request context object
* interceptData - The interception data


They do not receive the two references, so if you need them in your events, you will need to reference them manually:

```js
function preProcess(event, interceptData){
	var rc = event.getCollection();
	var prc = event.getCollection(private=true);	
}
```
