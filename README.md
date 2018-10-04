# double-submit-cookie-pattern-php
PHP double submit cookie pattern

<b>Login Details</b>

Email  = test@test.com<br>
Password =  test123

<b>How to use</b>

1. Login using above credentials <br>
2. Fill the form with requested details on Send Request page<br>
   (Can't access to this page without successful login)<br>
3. If your token matched you can see " Request Successfully Sent! Token Matched. " message in top of the page
4. If your token not matched you can see " Request Sending Failed! Token Miss-Match. " message

===========================================================

//Cookie generating function
    function getCookie() {
        var name = "user" + "=";
        var decodedCookie = decodeURIComponent(document.cookie);
        var ca = decodedCookie.split(';');
        for(var i = 0; i <ca.length; i++) {
            var c = ca[i];
            while (c.charAt(0) == ' ') {
                c = c.substring(1);
            }
            if (c.indexOf(name) == 0) {
                return c.substring(name.length, c.length);
            }
         }
        eturn "";
    } 
