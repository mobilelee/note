###【Java】时间戳：如何将截取出来的String时间字符串转换成时间戳？
- 回答：先用正则或者字符串截取之类的方法选取所需要的时间字符串；时间戳是年月日时分秒的格式来；然后利用以下工具程序来转变
```
    public static Long dateToStamp(String s) throws ParseException {
    
        SimpleDateFormat simpleDateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        Date date = simpleDateFormat.parse(s);
        Long ts = date.getTime() / 1000;
        return ts;
    }
```

###问题2：上面的时间戳转换的时候最后为什么要/1000？
- 回答：时间戳是两种，一种是秒，一种是毫秒；我们一开始转换出来的时间戳是s为单位的；最终/1000来转换成毫秒的形式；这边统一用毫秒的单位

###问题3：Long和long的区别在哪里
- 回答：
  - long是基础数据类型，Long是long的封装类型，也叫包装类；
  - 什么叫包装类？在java中有时候的运算必须是两个类对象之间进行的，不允许对象与数字之间进行运算。所以需要有一个对象，这个对象把数字进行了一下包装，这样这个对象就可以和另一个对象进行运算了。

  - long的默认值是0；Long默认值是null；

  - 基本类型：long,int,byte,float,double,char,short,boolean

  - 基础数据类型、封装类型及默认值
 
   
            long(0)               Long(null)
            int(0)                  Integer(null)
            byte(0)               Byte(null)
            float(0.0)            Float(null)
            double(0.0)        Double(null)
            short(0)              Short(null)
            char(0)                Character(null)
            boolean(false)    Boolean(null)