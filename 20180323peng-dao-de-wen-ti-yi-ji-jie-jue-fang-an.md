###【Java】时间戳：如何将截取出来的String时间字符串转换成时间戳？
####回答：先用正则或者字符串截取之类的方法选取所需要的时间字符串；时间戳是年月日时分秒的格式来；然后利用以下工具程序来转变
```
    public static Long dateToStamp(String s) throws ParseException {
        String res;
        SimpleDateFormat simpleDateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        Date date = simpleDateFormat.parse(s);
        Long ts = date.getTime() / 1000;
        return ts;
    }
```