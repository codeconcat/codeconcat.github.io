---
layout: post
title:  EventSouring Pattern
date:   2016-04-27 11:00:00 +0700
categories: pattern
header-img : /img/cbm4.png
excerpt : EventSourcing.
---
### I. ActiveRecord vs EventSourcing


#### What is an event ?
**Event** là một sự kiện diễn ra (vd : bỏ hàng vào giỏ, đặt hàng, thanh toán ... )

#### EventSouring thì như thế nào ?
+ Save những **events** dẫn đến **current state**, chứ k lưu **current state**
    * mở tài khoản => thêm $5 => rút $2 ( current state : $3 ) và mỗi hành động kia là 1 **event**
+ Append only - giống như cuộc sống, sự kiện đc diễn ra liên tọi.
+ Immutable - Sự kiện thì không thay đổi được ( k thế sửa `thêm $5` thành `thêm $3` được )

#### Advantages / Disadvantages
+ Log every changes 
+ Debug, trace

+ Steep learning curve - phải thay đổi cách nhìn nhận, xử lý vấn đề.
+ Ít framework, cộng đồng hỗ trợ

#### How does ES work 
+ Tạo ra 1 sự cho mỗi thay đổi state của object
+ Sử lý steam of events theo 1 thứ tự nào đó ( thường là tăng dần về thời gian)

#### When to use
 


##### Tham khảo :
+ [Promise - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
+ [http://callbackhell.com](http://callbackhell.com)

