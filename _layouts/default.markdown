<!DOCTYPE html>
<html>

  {% include head.html %}

  <body class="{{page.layout}}-layout">
    <!-- <div class="bg"></div> -->

    {% include header.html %}

        {{ content }}

    {% include footer.html %}


    {% if page.title contains "Zine" %} 
        <script>
          function getCookie(cname) {
          let name = cname + "=";
          let ca = document.cookie.split(';');
          for(let i = 0; i < ca.length; i++) {
            let c = ca[i];
            while (c.charAt(0) == ' ') {
              c = c.substring(1);
            }
            if (c.indexOf(name) == 0) {
              return c.substring(name.length, c.length);
            }
          }
          return "";
        }

        function setCookie(cname, cvalue, exdays) {
          const d = new Date();
          d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
          let expires = "expires="+d.toUTCString();
          document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
        }

          var form = document.querySelector('form.mc-form');
          var button = document.querySelector('form.mc-form button');
          let popUpCooke = getCookie("popUpSeen");
          let popUpSubmitted = getCookie("popUpSubmitted");
          var response = document.querySelector('#mce-success-response');
          var zineEmail = document.querySelector('.zine-email');
          var pageBlocker = document.querySelector('.page-blocker');
          if(popUpSubmitted == "true") {
              zineEmail.classList.add('hide');
              pageBlocker.classList.add('hide');
          }
          console.log(form);
          button.addEventListener('click', function(){
            console.log('click');
            setTimeout(function(){
              if(response.innerHTML === "Thank you for subscribing!") {
              console.log('done')
              zineEmail.classList.add('hide');
              pageBlocker.classList.add('hide');
              setCookie("popUpSubmitted", true, 999)
              } else {
                console.log('not subscribed');
              }
            }, 1500)
          });
        </script>
    {% endif %}
  </body>

</html>
