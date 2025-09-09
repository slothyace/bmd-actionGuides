# Evaluate
![](https://github.com/slothyace/bmd-actionGuides/blob/main/.images/evaluate.png)

## What does evaluate do?
`Evaluate` runs Javascript code.

## Example
```js
let approvedServers = bridge.variables[`approvedServerList`]
let allServers = bridge.variables[`botGuildIds`]

unapprovedServers = allServers.filter(server => !approvedServers.includes(server))
```

What this does is that it references 2 temporary variables and filters for servers that are not in the `approvedServers` list.

## Referencing Variables
To reference `Temporary` variables;
```js
let foo = bridge.variables["..."]
```

To reference `Server` variables;
```js
let foo = bridge.data.serverVars["serverId"]["..."]
```

To reference `Global` variables;
```js
let foo = bridge.data.globalVars["..."]
```

## Whats the difference between `Execute` and `Evaluate`?
`Execute ` - Runs **operating system** commands.<br>
`Evaluate` - Run **Javascript** code.
