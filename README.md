# js-prototype-
js 原型链 


      Pres.prototype.lasname="张三";
          function Pres(){
          }
       var pres=new Pres()
       Koo.prototype=pres;
       function Koo(){
         this.name="李四"
       }
       var koo=new Koo()
    
    Son.prototype=koo;
    function Son(){
    	this.names="王五"
    }
    
     var son=new Son()
        son.name   //李四
        son.names  //王五
        son.lasname  //张三
       
       
       
 Object.create()  也可以创建对象 ,但是这个对象是没有原型的
       
    语法 Object.create(原型  或者 null)
   
      1)  var obj=Object.create(null)
           console.log(obj)   //{}  空对象里面什么都没
       
     2)  
           var objTest={
            	name:"詹三"
           }
          var obj1=Object.create(objTest)
       
           console.log(obj1.name)  //詹三
           console.log(obj1)// {__proto__:
           	                //name: "詹三"
           	                // __proto__: Object为是么这个里面有__proto__ 可以访问原型链？那是因为objTest有原型链
                            //}
       
    3)      
          function Test2(){
          	
          }
        var test2=new Test2();
        var protos=Object.create(Test2.prototype)
       
         console.log(protos)    //{__proto__: Object}   这里他引用了Test2原型链
       





