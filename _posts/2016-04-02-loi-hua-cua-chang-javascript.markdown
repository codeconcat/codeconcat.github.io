---
layout: single
title      : Lời hứa của chàng Javascript - P1
date       : 2016-04-02 11:52:58 +0700
categories : javascript
header:
  overlay_color: "#333"
excerpt : Promise đối với async process
---
### I. Bài toán đi xem film
Một ngày đẹp trời, bạn muốn đi coi film, có nhiều film và nhiều gái nên bạn phải làm 1 service để lấy list film gửi cho list gái rồi nó sẽ cho bạn 1 list gái muốn đi xem nào để lựa ak.

Bạn cứ không cần quan tâm logic là thế nào hay code vậy có đúng, hay [http://getListGai.net](http://getListGai.net) làm gì tồn tại đâu, bày trò và cố tình viết xấu vậy để demo cho khái niệm **Callback Hell** hay **Pyramid of Doom** thôi mà. ( vào đây coi thêm ha : [CallbackHell](http://callbackhell.com)

Vì cái trên nhìn chướng mắt, nên ở đâu có sinh ra 1 thứ gọi là **Promise** để xử lý đống Async, thật ra thì còn nhiều kỹ thuật nữa, mà mình thì chưa biết hết được (Generator/yeild ở ES6, async/await ở ES7 ... ).

Một **Promise** thì từ sẽ trạng thái **Pending** ban đầu rồi có lúc sẽ chuyển thành 1 trong 2 trạng thái :

- **fulfilled** : meaning that the operation completed successfully.
- **rejected** : meaning that the operation failed.

Nhìn code thì nhiều dòng hơn, nhưng mà nhìn đi đỉ phải không, mình vì thế có thể viết cái đống

<pre><code class="js">getListFilms()
  .then(getListGais)
  .then(guiListFilmChoListGai)
  .then(traVeKetQuaCuoiCungNe)
  .catch(console.log)
</code></pre>

Giống cái này ha [Human centipede](https://www.google.com/url?sa=i&amp;rct=j&amp;q=&amp;esrc=s&amp;source=imgres&amp;cd=&amp;cad=rja&amp;uact=8&amp;ved=0ahUKEwjCrcjk8IrLAhWkdKYKHW9JDXAQjRwIBw&amp;url=http%3A%2F%2Fgoogle.com%2Fsearch%3Ftbm%3Disch%26q%3DThe%2520Human%2520Centipede&amp;psig=AFQjCNG3kIOmVJXvqcHACzMPqlHcm5SSmw&amp;ust=1456213667220289).

reject(err)` và `catch()` nó sẽ giúp mình handle error ở 1 nơi thôi, k còn phải handle trong từng cái callback nữa, và ngoài những err mình reject, bất kỳ lỗi nào phát sinh sẽ được cái catch nó catch lại, khỏi lo **err** nữa

#### Update 01 :

Promise trong JS còn có trò **all** sẽ chạy callback khi tất cả các Promise resovle, trả về array các return data của từng **Promise**

<pre><code class="javascript">Promise.all([getListFirms, getListGais])
.then((results) => {
  // results [ listFirms, listGais ]
})</code></pre>

Đón xem phần sau để biết thêm về `Promise.all` nhé.

##### Tham khảo :
+ [Promise - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
+ [http://callbackhell.com](http://callbackhell.com)

