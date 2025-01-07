
# نام آزمایش :
ایجاد انیمیشن ساده با استفاده از کاراکترهای سفارشی روی نمایشگر LCD


  ## شرح آزمایش :
در این آزمایش، ما دو کاراکتر سفارشی به شکل یک آدمک با دست‌های بالا و پایین ایجاد می‌کنیم. سپس با استفاده از حلقه‌های for و تغییر موقعیت مکان‌نما، این کاراکترها را به صورت متناوب در سطرهای مختلف نمایشگر حرکت می‌دهیم تا یک انیمیشن ساده ایجاد شود.
  

  ## کد آزمایش :
  #include <LiquidCrystal.h>

const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;

LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

byte heart[8] = {

  
  0b00000,
  
  0b01010,
  
  0b11111,
  
  0b11111,
  
  0b11111,
  
  0b01110,
  
  0b00100,
  
  0b00000

};

byte smiley[8] = {

  0b00000,

  0b00000,
  
  0b01010,
  
  0b00000,

  0b00000,
  
  0b10001,
  
  0b01110,
  
  0b00000

};


byte frownie[8] = {

  0b00000,
  
  0b00000,
  
  0b01010,
  
  0b00000,
  
  0b00000,
  
  0b00000,
  
  0b01110,
  
  0b10001

};


byte armsDown[8] = {

  0b00100,
  
  0b01010,
  
  0b00100,
  
  0b00100,
  
  0b01110,
  
  0b10101,
  
  0b00100,
  
  0b01010

};


byte armsUp[8] = {

  0b00100,
  
  0b01010,
  
  0b00100,
  
  0b10101,
  
  0b01110,
  
  0b00100,
  
  0b00100,
  
  0b01010

};


void setup() {

  lcd.begin(16, 2);
  
  lcd.createChar(0, heart);
  
  lcd.createChar(1, smiley);
  
  lcd.createChar(2, frownie);
  
  lcd.createChar(3, armsDown);
  
  lcd.createChar(4, armsUp);
  
  lcd.setCursor(0, 0);
  
  lcd.print("I ");
  
  lcd.write(byte(0)); 
  
  lcd.print(" Arduino! ");
  
  lcd.write((byte)1);


}

void loop() {

  int sensorReading = analogRead(A0);
  
  int delayTime = map(sensorReading, 0, 1023, 200, 1000);
  
  lcd.setCursor(4, 1);

  lcd.write(3);
  
  delay(delayTime);
  
  lcd.setCursor(4, 1);
  
  lcd.write(4);
  
  delay(delayTime);

}


 
  
  ## تفسیر کد:
دو حلقه for برای ایجاد حرکت کاراکترها در دو جهت مختلف استفاده شده است. در هر تکرار حلقه، مکان‌نما در یک موقعیت جدید قرار می‌گیرد و کاراکتر مربوطه نمایش داده می‌شود. با استفاده از تابع delay، بین هر تغییر موقعیت، یک مکث کوتاه ایجاد می‌شود تا انیمیشن روان‌تر به نظر برسد.
  



## خروجی آزمایش:
![alt text](https://github.com/Rahel12384/Microprocessor-5/blob/main/micro%201%20/%20Report%203%20/%20VID_20250106_173813_844%20(1).gif)

  
## نتیجه گیری:


