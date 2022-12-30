# Second Assignment

### First Part
***
به متغییرهایی که در بدنه ی smart contract تعریف میشن، state variable میگن. این متغییرها میتونن داخل بدنه تعریف بشن یا اینکه متغییرهای تعریف شده داخل بلاکچین باشن مثل آدرس یا میزان موجودی کیف پول ها.
اگر تابعی این متغییرها رو تغییر نده و فقط این متغییرها رو بخونه بهش view function میگن.
 توابع pure توابعی هستند که نه تنها این متغییرها رو تغییر نمیدن، بلکه حتی این متغییرها رو نمیخونن و ازشون استفاده ای نمیکنن.
مثلا تابعی که از متغییرهایی که به عنوان ورودی میگیره استفاده کنه و یا متغییری در داخل بدنه تعریف کنه، این تابع همچنان pure هست.
مثلا تابع زیر که دو تا متغییر داخل بدنه تعریف شده و دو متغیر دیگه هم بر اساس دو متغییر اولیه تعریف شدن نمونه ای از توابع pure هست:

```
pragma solidity ^0.5.0;
 
contract PureTestFunction {
  
   function PureFunction() public pure returns(uint product, uint sum){
      uint num1 = 2; 
      uint num2 = 4;
      product = num1 * num2;
      sum = num1 + num2; 
   }
}
```
***
### Second Part
***
برای اینکه بتونیم بعد یا قبل از اجرای توابع مورد خاص یا شرط خاصی رو اجرا کنیم از modifier ها استفاده میکنیم.
که میتونیم بهشون ورودی هایی از همون ورودی های تابع اصلی یا هر ورودی دیگه ای بدیم و انتظار داشته باشیم که شرط یا کار خاصی رو برامون اجرا کنن.
برای استفاده از modifier ها میشه اونها رو بعد از تعریف تابع، و قبل از اسکوپ اصلی تابع نوشت و در خود طmodifier هم میشه هر جایی که میخواهیم تابع اجرا بشه، یه علامت _; بذاریم.
همچنین میشه از چندتا modifier استفاده کرد که باید به همون صورت قبلی فقط پشت هم نوشته بشن که من چون موارد مرتبط بودن، برای تابع آخر از یک modifier استفاده کردم.
***
لینک تراکنش برای ساخت کانترکت:
‍‍‍
https://goerli.etherscan.io/tx/0x3269619d1eef78162f5a5d8cb60c9882411d5e05505f7222ad66aca4d564cab9