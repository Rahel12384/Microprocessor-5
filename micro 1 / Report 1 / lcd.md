## نام آزمایش :
نمایش پیام روی نمایشگر LCD با استفاده از آردوینو


## توضیحات آزمایش:
در این آزمایش، ما از یک نمایشگر LCD 16x2 استفاده می‌کنیم تا دو پیام خوش آمدگویی را نمایش دهیم. برای این کار، از کتابخانه LiquidCrystal آردوینو استفاده خواهیم کرد که کار با LCD را بسیار ساده می‌کند.



## کد آزمایش :


#include <LiquidCrystal.h>

LiquidCrystal Lcd(12,11,5,4,3,2);

void setup() {


Lcd.begin(16, 2);

  Lcd.clear();

}

void loop() {

  
  Lcd.print("Hello world");
  
  Lcd.setCursor(0, 1);
  
  Lcd.print("lcd Tutorial");

}


## تفسیر کد:

#include <LiquidCrystal.h>: این خط کتابخانه LiquidCrystal را به برنامه اضافه می‌کند.

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);: این خط یک شیء از کلاس LiquidCrystal ایجاد می‌کند و پین‌های اتصال LCD به آردوینو را مشخص می‌کند. این پین‌ها ممکن است در بردهای مختلف متفاوت باشند. lcd.begin(16, 2);: این دستور ابعاد LCD را تنظیم می‌کند.

lcd.clear();: این دستور صفحه LCD را پاک می‌کند. lcd.setCursor(x, y);: این دستور مکان نما را در ستون x و سطر y قرار می‌دهد. lcd.print("متن");: این دستور متن مورد نظر را در مکان نما فعلی چاپ می‌کند.



## خروجی ازمایش:
![توضیح تصویر](https://github.com/Rahel12384/Microprocessor-5/blob/main/micro%201%20/%20Report%201%20/%20IMG_20250106_173750_350.jpg)
