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

function sniff(o,caller){o= new Proxy(o,{ set:(oo,k,v)=>{return caller(oo,k,v),oo[k]=v } }) }
sniff(t,(o,k,v)=>{
 console.log(k,v)
 if(!(k==='loadedflg'&&v))return;
 
})
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
/*



 function tilecalc(d,size){
 ///
  let f=(ctx,size)=>{
  let oImgData = ctx.getImageData(0, 0, size, size);
  let canvas=document.createElement('canvas')
  canvas.width=canvas.height=size
  let wk=canvas.getContext('2d')
    wk.putImageData(oImgData, 0, 0);
    return wk.canvas.toDataURL()
 }
 ///
 let canvas=document.createElement('canvas')
 canvas.width=canvas.height=size
 let ctx=canvas.getContext('2d'),image=d,size=o.size
 let cellw=parseInt(image.naturalWidth/size)
 let cellh=parseInt(image.naturalHeight/size)
 let ary=[]
 for(let y=0;y<cellh;y++)
  for(let x=0;x<cellw;x++){
    ctx.drawImage(image, x*size, y*size, size, size, 0, 0, size, size);
    let src=f(ctx,size);
    let im=new Image();im.src=src
    ary.push(im)
  }
 return ary;
 }


let fn={};fn.ce
let me={}
me.loadTile=(url,size)=>{return new Promise(sol=>{
 let d=fn.ce('img'),type='tile'
 d.crossOrigin = "Anonymous"; 
 d.onload=()=>{
  let ary=tilecalc(d,size)
  return sol({url:url,name:url.split('/').pop(),type:type,data:ary,str:'',base64:''})
 }
 d.src=url;
}}
me.loadImg=(url)=>{return new Promise(sol=>{
 let d=fn.ce('img'),type='bgm'
 d.crossOrigin = "Anonymous"; 
 d.onload=()=>{return sol({url:url,name:url.split('/').pop(),type:type,data:d,str:'',base64:''})}
 d.src=url;
}}
me.loadBgm=(url)=>{return new Promise(sol=>{
 let d=fn.ce('video'),type='bgm'
 d.crossOrigin = "Anonymous";  
 d.onload=()=>{return sol({url:url,name:url.split('/').pop(),type:type,data:d,str:'',base64:''})}
 d.src=url;
}}
me.loadSe=(url)=>{return new Promise(sol=>{
 let d=fn.ce('video'),type='se'
  d.crossOrigin = "Anonymous"; 

 d.onload=()=>{return sol({url:url,name:url.split('/').pop(),type:type,data:d,str:'',base64:''})}
 d.src=url;
}}
me.loadJson=(url)=>{
 return fetch(url)
 .then(d=>d.json())
 .then(d=>{return {url:url,name:url.split('/').pop(),type:'json',data:d,str:'',base64:''} }
}
;
me.loadTxt=(url)=>{
 return fetch(url)
 .then(d=>d.text())
 .then(d=>{return {url:url,name:url.split('/').pop(),type:'txt',data:d,str:'',base64:''} }
}
;
me.r['name'] {url,name,type,data,str,base64} //name =>xyz.png
me.t0=performance.now();

let f=(d)=>{
 function _c(d){return d.replace(/\/\*[\s\S]*?\*\/|([^\\:]|^)\/\/.*$/gm,'')}
 return _c(d.trim())
}

Promise.resolve(f(me.str).split('\n').map(d=>{
try{
 let a=d.split(','),type=d[1]
 if(type==='tile')return me.loadTile.bind(a[0],parseInt(a[2]))
 if(type==='img')return me.loadImg.bind(a[0])
 if(type==='bgm')return me.loadBgm.bind(a[0])
 if(type==='se')return me.loadSe.bind(a[0])
 if(type==='json')return me.loadJson.bind(a[0])
 if(type==='txt')return me.loadTxt.bind(a[0])
 return console.log('unkown type',d),void 0
}catch(e){return console.log('unkown type',d),void 0}
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



