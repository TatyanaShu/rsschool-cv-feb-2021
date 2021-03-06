![my photo](assets/IMG_20200912_120604.jpg)
My name is Tatyana Shuniborova.
I live in Minsk, Belarus.
My telephone number: +375-29-863-88-11
Other communication methods: viber/telegram +375-29-863-88-11
Content:
1. [About me](#about)
2. [Skills](#skills)
3. [Example code](#example)


<a id="about">___About me___</a>
I am studying in Institute of business BSU on web-design.  I am studying some languages of programming as:  HTML5, CSS3, JavaScript. 
On the lessons of JavaScript we are studying native JavaScript, jQuery and some features of animation.
I finished study some graphic program such as: Photoshop, corel, adobe animation and 3ds max.
I studied English at last year, and I want to learn this language more. I graduated some curses of English as: elementary and pre-intermediate levels.
I was start  to learn programming in last year and I will graduate it in September at this year.
I work in another  sphere, and I don’t like it. I want to try something else, I like computers  and to do  some interesting things and see results, which useful for people.
I am purposeful and i like  to fulfills  my plans.

---

<a id="skills">__Skills:__</a>
* HTML5.0;
* CSS3.0;
* JavaScript;
* jQuery;
* SQL;
* graffiti programs:
  * Corel;
  * PhotoShop;
  * AdobeAnimation.

---

<a id="example">__Example code:__</a>
```
_//счетчик  цифр на 2 странице_
const timeCount = 10000,
  step = 20;
function outNum(num, elem) {
  let numb = document.querySelector("#" + elem);
  n = 0;
  let timeView = Math.round(timeCount / (num / step));
  let interval = setInterval(() => {
    n<num? (n += step): clearInterval(interval);
    numb.innerHTML = n;
  }, timeView);
}
_// валидация формы регистрации_
function validate() {
  let errList=document.querySelectorAll ("span");
  let userName=document.getElementById('userName');
  console.log(userName);
  let userPhone=document.getElementById('userTelephone');
let item=document.createElement("span"); 
item.innerHTML ="Поле обязательно для заполнения";
  for (let i= errList.length-1; i>=0; i--) {
        errList[i].remove();
    }
    if (!userName.value){
    userName.classList.add("errorList");
    userName.parentNode.insertBefore(item,userName.nextSibling);
    return false;
    } else{
    userName.classList.remove("errorList");
    item.remove();
  }
  if (!userPhone.value){
    userPhone.classList.add("errorList");
    userPhone.parentNode.insertBefore(item,userPhone.nextSibling);
    return false;
  }
  else{
    userPhone.classList.remove("errorList");
    item.remove();
  }
    
    form=document.entered;
    let login=isFullText(userName);
    let phone=isPhone(userPhone);
    return login&& phone;
}
function isFullText(fieldInp) {
  var letters = /^[A-Za-z]+$|^[А-Яа-я]+$/;

  if (fieldInp.value.match(letters)) {
    fieldInp.className = fieldInp.className.replace("alert", "");
    return true;
  } else {
    fieldInp.className = "alert";
    var item = document.createElement("span");
    item.innerHTML = "Имя должно состоять из букв латиницы или кириллицы";
    fieldInp.parentNode.insertBefore(item, fieldInp.nextSibling);
    return false;
  }
}

function isPhone(userPhone) {
  var pattern = /^(\+\d{3})(\d{2})(\d{3})(\d{2})(\d{2})$/;
  if (userPhone.value.match(pattern)) {
    userPhone.className = userPhone.className.replace("alert", "");
    return true;
  } else {
    userPhone.className = "alert";
    var item = document.createElement("span");
    item.innerHTML = "Телефон должен быть формата +375...";
    userPhone.parentNode.insertBefore(item, userPhone.nextSibling);
    return false;
  }
}
```
