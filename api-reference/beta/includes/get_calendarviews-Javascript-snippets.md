
```Javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups/02bd9fd6-8f93-4758-87c3-1fb73740a315/calendarView')
    .version('beta')
    .header('Prefer','outlook.body-content-type="text"')
    .get();

```