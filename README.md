## Prettify Javascript's object
```javascript
function rec(obj, gen=0){
  strip=""
  for(i of [...Array(gen).keys()]){
    strip+="  "
  }
  for(key in obj){
    a=strip
    b=key
    idr=obj[key].constructor.name
    idr=="Object" ? c="" : c=`- ${obj[key]}`
    console.log(a+b+c)
    if(c==""){
      rec(obj[key],gen+1)
      rec(obj[key],gen)
    }
  }
}
```
```bash
aitem
  aaitem
    aaaitem
      twok - 2000
      array - 0,0,0
    aaaitem2 - hai
  aaitem2 - hi
bitem
  bbitem - think
citem - 17
```
