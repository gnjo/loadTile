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
t.loading//debug
```

```
let da=rs(`
https://gnjo.github.io/image2.png,tile,16
https://gnjo.github.io/image4.png,img
https://gnjo.github.io/video.ogg,bgm
https://gnjo.github.io/shot.ogg,se
https://gnjo.github.io/mapdata.json,json
https://gnjo.github.io/xyz.md,txt
`,(me)=>{
 let arys=me.get('image2.png','tile') //ary
 let d=me.get('image2.png','img')
 let d=me.get('image4.png','se')
 
 //if namesymbol not some//quick
 me.get('image2',type)  //return data
 me.getObject('')
})
me.loadTile
me.loadImg
me.loadBgm
me.loadSe
me.loadJson
me.loadTxt
me.r['name'] {url,name,type,data,str,base64} //name =>xyz.png
me.pary=[]
me.t0=performance.now();
/*

Promise.resolve(me.str.split('\n').map(d=>{
 let a=d.split(','),type=d[1]
 if(type==='tile')return me.loadTile.bind(a[0],a[2])
 if(type==='img')return me.loadImg.bind(a[0])
 if(type==='bgm')return me.loadBgm.bind(a[0])
 if(type==='se')return me.loadSe.bind(a[0])
 if(type==='json')return me.loadJson.bind(a[0])
 if(type==='txt')return me.loadTxt.bind(a[0])
 return console.log('unkown type',d),void 0
}).filter(d=>d))
.then(Promise.all)
.then(d=>{ 
  me.r[d.name]=d;
  me.loadedflg=true;
  me.loading='complete'
  me.time=performance.now() - me.t0
  console.log(me.time,Object.keys(me.r).length)
})
*/
```



