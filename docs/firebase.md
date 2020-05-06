# Firebase

## Environment Config

### Set
```bash
firebase functions:config:set someservice.key="THE API KEY" someservice.id="THE CLIENT ID"
```

### Get
```bash
functions:config:get
```

### Access
```javascript
functions.config().someservice.key
```

### Remove
```bash
firebase functions:config:unset key1 key2
```

### Clone
```bash
firebase functions:config:clone --from <fromProject>
```