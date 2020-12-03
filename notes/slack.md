<!-- njnmdoc:  title="slack"  -->

## Dumping slack's DB

To extractr the local database for slack from the web client, you can use the below snippet + the console.save script.

```
window.indexedDB.open("reduxPersistence",2).onsuccess = function(event){
    const rps = "reduxPersistenceStore";
    const id = "persist:slack-client-T015X27QLAF-U0177NKS3LN";
	var db = event.target.result;

	db.transaction(rps, "readonly").objectStore(rps).get(id).onsuccess = function(event) {
		var data = event.target;
		console.save(data.result)
    }
}
```

## Custom UCLA Theme

```
#2774AE,#FFF8D4,#2774AE,#FFB81C,#003B5C,#FFFFFF,#003B5C,#2774AE,#FFD100,#003B5C
```

