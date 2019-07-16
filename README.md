# MMVAS REST API 

## API BASE URL

آدرس وب سرویس اعتبارسنجی کاربران به شرح زیر است. با توجه به نوع پلتفرم پیاده سازی درگاه، از یکی از دو آدرس زیر استفاده کنید

***Api Base Url*** 

        ``http://s1.mmvas.ir/api/vas/{serviceId}``

serviceId :
شناسه سرویس را از طریق تماس با پشتیبانی دریافت کنید

## LOGIN
* [Login](pushOtp.md) : `POST /otp/request`

## VERIFY
* [Verify](chargeOtp.md) : `POST /otp/charge`

## CHECK USER SUBSCRIPTION STATUS
* [Check Subscription](checkSub.md) : `GET /subscription/check`

## UNSUBSCRIBE USER
* [Unsubscribe](unsub.md) : `POST /unsubscribe`

