<!-- njnmdoc:  title="slack"  -->

## Dumping slack's DB

To extractr the local database for slack from the web client, you can use the below snippet + the console.save script.

```
window.indexedDB.open("reduxPersistence",2).onsuccess = function(event){
    const rps = "reduxPersistenceStore";
    const id = "persist:slack-client-" + document.querySelector("div.p-ia__nav__user > span > img").src.replace(/.*\//, '').replace(/-[0-9a-z]*-[0-9]*$/, '');
	var db = event.target.result;

	db.transaction(rps, "readonly").objectStore(rps).get(id).onsuccess = function(event) {
		var data = event.target;
		console.save(data.result)
    }
}
```

To convert to contacts format using jq:

```
jq -r '["First Name","Last Name", "Email Address","Real Name"], (.members[].profile | {first_name, last_name, email, real_name} | [.[]]) | @csv'

```

## Custom UCLA Theme

```
#2774AE,#FFF8D4,#2774AE,#FFB81C,#003B5C,#FFFFFF,#003B5C,#2774AE,#FFD100,#003B5C
```

