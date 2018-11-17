# MMVAS REST API 

## API BASE URL

آدرس وب سرویس اعتبارسنجی کاربران به شرح زیر است. با توجه به نوع پلتفرم پیاده سازی درگاه، از یکی از دو آدرس زیر استفاده کنید

Api Base Url 
  - IMI : 
        `http://s1.mmvas.ir/api/imi/{serviceId}`
  - Pardis : 
        `http://s1.mmvas.ir/api/pardis/{serviceId}`

serviceId : is the unique ID for VAS service you want to use.

شناسه سرویس را از طریق تماس با پشتیبانی دریافت کنید

## LOGIN
* [Login](pushOtp.md) : `POST /otp/request`

## VERIFY
* [Verify](chargeOtp.md) : `POST /otp/charge`

## CHECK USER SUBSCRIPTION STATUS
* [Check Subscription](checkSub.md) : `GET /subscription/check`

## UNSUBSCRIBE USER
* [Unsubscribe](unsub.md) : `POST /unsubscribe`

