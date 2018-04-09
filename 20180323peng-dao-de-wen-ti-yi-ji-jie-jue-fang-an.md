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