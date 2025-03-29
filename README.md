<h1>
مبهم کننده کدهای جاوااسکریپت
<br>
  
Obfuscating JavaScript codes to set up an app on a specific site
</h1>

فرض کنید بخواهید یک نرم افزار تحت وب را بفروشید و کسی نتواند آن را در آدرس دیگر راه اندازی کند.
<br><br>

Suppose you want to sell a web application and no one can launch it anywhere else.
<br><br>

![Screenshot_۲۰۲۵۰۳۲۹-۱۴۲۴۰۰_Chrome](https://github.com/user-attachments/assets/7b3f6daf-2d45-431d-922a-6eb2cff23a87)



اگر کدی شبیه کد زیر داشته باشید می توانید آن را به کمک این برنامه مبهم کنید تا کسی آن را پیدا نکند.
<br><br>
```javascript
function checkDomain() {
    const allowedDomain = "yourdomain.com"; 
    const currentDomain = window.location.hostname;
    if (currentDomain !== allowedDomain) {
        document.body.innerHTML = "<h1> Access Denied: Invalid Domain </h1>";
        return false;
    }
    return true;
}
window.onload = function() {
    if (!checkDomain()) {
        return;
    }
    console.log( "Welcome to the allowed domain!" );
};
```
