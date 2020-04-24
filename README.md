# loadTile
```
//usage
let t=loadTile(`
https://gnjo.github.io/image2.png,16 //t['image2'][0]
https://gnjo.github.io/image3.png,32 //t['image3'][0]
https://gnjo.github.io/image4.png //t['image4'][0] //one only

`,caller);
function caller(me){
 let ary=me['image2']
 ary.map(el=>{ document.body.appendChild(el) }
 console.log(me.time,me.loadedflg)
}
t.isis(key)
t.isloaded()
t.loadedflg=false
t.time
```
