---
layout: single
title:  Microservices - Know the Monolithic 
date:   2016-05-04 16:52:58 +0700
categories: architecture
header:
  overlay_image: cbm4.png
  overlay_color: "#333"
excerpt : Before Microservices there were Monolithic
---
# Life before Microservices - Monolithic
Phần lớn những service, server, webapp hiện tại đang được làm dưới dạng **Monolithic architecture**

+ Tất cả xử lý sẽ được đóng gói trong 1 **codebase** duy nhất.
+ Sản phẩm cuối cùng của project bạn có thể là :
    - 1 file chứa toàn bộ source code ( vd : war (Java) )
    - 1 directory chứa source code ( vd : NodeJs, Php, Ruby directory )

Đây là ví dụ rất rõ ràng và trực quan trên [nginx](https://www.nginx.com/blog/introduction-to-microservices/) về **monolithic architecture**

+ Phần **Core** của Application (cái hình lục giác đó) sẽ định nghĩa các Services các xử lý logic của  applicaiton
+ Bao quanh nó sẽ có các thành phần để tương tác với bên ngoài ( như connect DB via MYSQL Adapter, expose REST API, provide WebUI  ... )

![Monolithic](https://assets.wp.nginx.com/wp-content/uploads/2016/04/Richardson-microservices-part1-1_monolithic-architecture.png)

### Advantages of monolithic :
+ Quen thuộc đối với phẩn lớn developer
+ Dễ dàng cho việc phát triển ( nhiều IDE, framework, tools hỗ trợ )
+ Dễ dàng Test
+ Dễ dàng khi deploy ( single codebase )

### Disadvantages of monolithic :
+ Hard to scale, khi mà các modules có **strong coupling**.
+ **LOC** sẽ tăng vèo vèo khi scale, readability sẽ tụt tùn tụt
+ Project theo hướng **Agile development** sẽ gặp rất nhiều khó khăn khi **complexity** tăng, quá khó cho 1 developer có thể hiểu hoàn toàn 1 cấu trúc lớn và phức tạp như vậy.
+ Khó khăn khi thực hiện **countinous deployment**, việc **push changes to product** được thực hiện nhiều lần trong ngày, đối với **monolithic** sẽ redeploy lại toàn bộ application, chỉ để apply 1 phần thay đổi của application đó.
+ Không có độ linh hoạt trong việc **choose the right tool for the right job**, ví dụ : bạn có 1 application 10000 LOC viết bằng framework ABC, giờ có 1 số modules bạn muốn viết lại bằng framework XYZ, impossible !

### Solution ?
**Microservices** is here for the rescue ( in the next chaper 😎 )

Cảm ơn và tham khảo nè:

+ [Microserives - nginx](https://www.nginx.com/blog/introduction-to-microservices)

