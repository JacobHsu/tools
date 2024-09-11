# Automa

Loop data  + 中斷點  
insert data 字串要用雙引號
["2-1","2-2"]

`?INDUSTRY_CAT={{loopData@h4i43i}}`  

JavaScript Code  
```
console.log(automaRefData('loopData', 'h4i43i').data);
automaNextBlock()
```



[Global data](https://docs.automa.site/workflow/global-data.html)  
```
{
	"key": "value", "myid": "666"
}
```

Text field
```
global id {{globalData.myid}}  
```


[Fill Form by Google sheet in Automa | Automa](https://www.youtube.com/watch?v=Zuk6fBc2EjE&list=PLBW9VlVpFr4y3NkZjp0O5SsUMAnwaX171&index=3)

JavaScript Code  

```
automaSetVariable('name', 'Jacob')
automaNextBlock()
```

Forms  

Text field
```
My name is {{variables@name}}
```


### Example

notebooklm

copy icon
`.actions-container .rhs-start .mat-icon`

Get Text  
`mat-card-content.to-user-message-inner-content`
