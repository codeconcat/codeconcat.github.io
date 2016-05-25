---
layout: post
title:  A useful CAPSLOCKS
date:   2016-04-27 11:52:58 +0700
categories: tips
image: http://www.howtogeek.com/wp-content/uploads/gg/up/xsshot4d0bb21e1804e.jpg.pagespeed.gp+jp+jw+pj+js+rj+rp+rw+ri+cp+md.ic.0fRzh_qKvO.jpg
---
Bọn **Developer** lông hôi thì, mỗi tên lại có **stack** riêng, [Check MeoBeoI stacks](http://stackshare.io/MeoBeoI), khi làm thi thoảng cũng phải switch qua lại giữa các app ( software ... ), **thao tác** của bạn sẽ làm như thế nào ?

Một cô làm việc trên **Windows** :
+ Click vào icon trên destop
+ Click vào **pined app** ở **Taskbar**
+ **Pin app** vào <strong>taskbar </strong>rồi bấm <kbd><i class="fa fa-windows" aria-hidden="true"></i></kbd> + <kbd>1</kbd> <kbd>2</kbd><kbd>3</kbd> hay <kbd>Alt</kbd> + <kbd>Tab</kbd>

Một chú thao tác trên **MAC** :
+ <kbd>Cmd</kbd><kbd>Space</kbd> open **Spotlight** => **app name** => <kbd>enter</kbd>

Có thằng bạn khoe phím cơ 5 mê, không có nhiều phím, nó bảo

> Phím CAPS LOCK có bao giờ dùng đâu, chỉ toàn bấm nhầm vào thôi 

![Em nó đây](https://elitekeyboards.com/proddata/images/th/pdkb400b_full1000_th0x0.jpg)

Thấy cũng đúng, **dev** lông như mình thì cần gì **CAPLOCKS**, thế là hành trình biến đổi **CAPLOCKS** bắt đầu từ đây.

## Mục tiêu : Mở app nhanh với hotkey

### Step 1 : Tạo service để chạy app
1. Vào **Automator ==> Service**
2. **Launch Application** ( nhớ chọn "no input" như hình nha )
![step1-2](http://i.imgur.com/d3G4qgl.png)
3. Kéo cái **Launch Application** vào chỗ `Drag actions or files here to build your workflow` chứ gì nữa
4. Chọn Application, bấm nút play trên kia thử có được k nào .
5. Save lại với tên gợi nghĩa ( open Sublime, open Terminal ...)

Xong bước **"Tạo service để chạy app"**, giờ khi nào muốn mở Sublime thì vào service đó bấm play thôi hô hô, tiện quá chứ gì ( tiện éo đâu ra ???).

Đó là bước 1/3 thôi, nhanh nhanh nào, chúng ta cùng thiết lập **Shortcut** để chạy **Service** vừa rồi nào.

### Step 2 : Dùng shortcut để chạy service
1. Vào **Keyboard ==> Shortcut ==> Services**
2. Tùy vào trí tưởng tượng hay gì gì đó của bạn mà đặt **Hotkey** vào đó để chạy cái service đó, như mình thì chơi <kbd>F19</kbd> ( <kbd>shift</kbd> + <kbd>ctrl</kbd> + <kbd>alt</kbd> + <kbd>⌘</kbd> ) + <kbd>other key</kbd> 😼
![step2-2](http://i.imgur.com/w9zeL6m.png)
3. Giờ thì ra bấm thử đống phím đó cùng lúc xem có mở Sublime hay cái gì gì của chưa nào


### Step 3 : A useful CAPS LOCK
Để ý thì trên kìa có lan man về <kbd>caps lock</kbd> mà chưa thấy đâu, giờ là lúc vọc vẹo đến em nó rồi nè, bạn thấy để bấm đủ <kbd>shift</kbd> + <kbd>ctrl</kbd> + <kbd>alt</kbd> + <kbd>⌘</kbd> + <kbd>S</kbd> để mở Sublime nó tốn nhiều ngón tay chưa, giờ ý tưởng là Bấm <kbd>caps lock</kbd> + <kbd>S</kbd> là mở Sublime rồi, muốn được vậy thì phải biến <kbd>caps lock</kbd> thành **A useful CapsLock**

1. Down và install <a href="https://pqrs.org/osx/karabiner/index.html.en" target="_blank">Karabier</a>
2. **Open Karabier --> Misc & Uninstall --> <kbd>open private.xml</kbd>**
3. Paste của nợ này vào
<script src="https://gist.github.com/MeoBeoI/11ec42dd99ca06d40148.js"></script>
4. **Change Key**, checked **F19 to F19**

Xong rồi đó, nếu muốn chắc thì khởi động lại máy, chắc hơn thì cái lại Win luôn 

#### Lời tựa cuối
Hy vọng thay đổi nhỏ này sẽ giúp bạn có thể tự tin ra lệnh cho máy vi tính của mình, bắt nó làm theo ý muốn, người ngoài nhìn vào thấy hoành tráng, và chính nhất là **Nâng cao hiệu quả công việc**


#### Cảm ơn và tham khảo nè:

+ [Google - "a useful caps lock"](https://www.google.com/search?client=safari&amp;rls=en&amp;q=a+useful+caps+lock&amp;ie=UTF-8&amp;oe=UTF-8"target="_blank">)
+ [anh.at](http://anhd.at")

