---
layout: post
title:  EventSouring Pattern
date:   2016-04-27 11:00:00 +0700
categories: pattern
header-img : /img/cbm4.png
excerpt : EventSourcing.
---
### Lời nói đầu 


### I. ActiveRecord vs EventSourcing
+ **ActiveRecord (ORM)** là việc mapping 1 Class với 1 Database Table, như vậy 1 object instance sẽ được map với 1 record trong Database.
+ CRUD đối với Object sẽ được apply cho record trên database.

#### What is an event ?
+ **Event** là một sự kiện diễn ra (vd : bỏ hàng vào giỏ, đặt hàng, thanh toán ... )
+ **Event** xảy ra trong quá khứ.
+ **Event** là <span style="color: red;">Immutable</span>.

#### EventSouring thì như thế nào ?
+ Lưu tất cả các **events** xảy ra đối với một đối tượng, khi có tất các events, có thể **build lại bất cứ state** nào của đối tượng đó.
    * Mở tài khoản => thêm $100 => rút $20 => rút $30 ( **current state** : $50 )
+ Append only - giống như cuộc sống, sự kiện đc diễn ra liên tọi
+ Immutable - Sự kiện đã xảy thì không thay đổi được ( k thế sửa `thêm $100` thành `thêm $500` được )

#### Advantages
+ Có thể build lại hệ thống, object ở bất cứ state nào
+ Log every changes
+ Debug, trace
+ Easy to scale - thường ES được áp dụng CRQS, Segregate operations that Read and Update data by using separate interfaces


#### Disadvantages
+ Steep learning curve - phải thay đổi cách nhìn nhận, xử lý vấn đề.
+ Ít framework, cộng đồng hỗ trợ

#### When to use
 Have a lot of behaviour that is NOT CRUD
 Record events that occur
 Accountability / debugability / tracibility is critical
 Your domain is inherently event driven (ex : score tracking )
 You’re building a scaleable system based on CQRS pattern
 


##### Tham khảo :
+ [Promise - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
+ [http://callbackhell.com](http://callbackhell.com)

