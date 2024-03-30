## I. Wifi là gì?

WiFi, hay Wi-Fi, là một công nghệ cho phép thiết bị điện tử kết nối với một mạng không dây (WLAN) sử dụng sóng vô tuyến, cho phép trao đổi dữ liệu và kết nối internet mà không cần dùng đến dây kết nối vật lý. Tên "WiFi" không phải là viết tắt hay từ viết tắt của bất kỳ cụm từ chính thức nào; thực tế, nó là một thương hiệu được tạo ra bởi một công ty quảng cáo được thuê bởi WiFi Alliance, một tổ chức thương mại quốc tế, để làm cho tên "IEEE 802.11" - chuẩn kỹ thuật mà nó dựa trên - dễ nghe và dễ nhớ hơn.

Cơ chế hoạt động của WiFi dựa trên việc phát sóng vô tuyến. Một thiết bị, thường là một bộ định tuyến (router) hoặc điểm truy cập, sẽ phát sóng vô tuyến. Các thiết bị khác như máy tính, điện thoại thông minh, máy tính bảng, và các thiết bị thông minh khác có khả năng nhận và truyền dữ liệu qua những sóng này. Tùy thuộc vào loại bộ định tuyến và môi trường xung quanh, tín hiệu WiFi có thể phủ sóng trong một khu vực từ vài chục đến vài trăm mét.

WiFi hoạt động trên một số băng tần vô tuyến, chủ yếu là 2.4 GHz và 5 GHz. Mỗi băng tần có những đặc điểm khác nhau: băng tần 2.4 GHz có tầm phủ sóng rộng hơn và khả năng xuyên qua vật cản tốt hơn nhưng dễ bị nhiễu hơn, trong khi băng tần 5 GHz cung cấp tốc độ cao hơn và ít bị nhiễu hơn nhưng có tầm phủ sóng ngắn hơn và khả năng xuyên qua vật cản kém hơn.

Sự phổ biến của WiFi không ngừng tăng lên do sự tiện lợi và linh hoạt mà nó mang lại. Người dùng có thể kết nối nhanh chóng với internet ở hầu hết mọi nơi có sóng WiFi, từ nhà riêng, văn phòng, cà phê, sân bay, đến nhiều khu vực công cộng khác. Công nghệ này cũng là nền tảng cho nhiều ứng dụng hiện đại, từ điều khiển thiết bị thông minh trong nhà đến phát triển của các dịch vụ streaming trực tuyến, và là một yếu tố quan trọng trong sự phát triển của Internet vạn vật (IoT), nơi hàng tỷ thiết bị được kết nối và giao tiếp qua internet.

## II. Xác thực mật khẩu wifi diễn ra như thế nào?

WPA/WPA2:

![image](https://github.com/NVex0/An_Toan_Thuong_Mai_Dien_Tu/assets/113530029/6a2ac4f1-dfc8-4121-9278-e2e024847518)

Bước 1: thiết bị muốn truy cập WiFi (ví dụ như điện thoại, có thể gọi là Client) khi muốn truy cập tới router WiFi (có thể gọi là AP - Access Point) sẽ dò mạng và thấy sóng của router. Trong sóng phát thăm dò của router có mã ngẫu nhiên gọi là ANONCE, và điện thoại sẽ nhận lấy mã ANONCE.

Bước 2: điện thoại lấy mã ANONCE rồi tính toán ra một mã ngẫu nhiên khác gọi là SNONCE và gửi cho router kèm một số thông tin được mã hóa kèm SNONCE về danh tính và cả mật khẩu Wi-Fi.

Bước 3: router nhận được SNONCE thì sẽ biết được điện thoại gửi mật khẩu Wi-Fi đúng, từ đó router "hăm hở" gửi lại cho điện thoại mã khóa chung gọi là GTK (Group Temporal Key) để điện thoại dùng mã khóa này khi gửi thông tin cho router. Khi nhận được router sẽ biết mà giải mã.

Bước 4: điện thoại nhận được GTK sẽ lưu lại (Installation) rồi mã hóa một tín hiệu ACK gửi lại cho router để báo hiệu đã nhận được khóa. Rồi từ đó 2 phía nói với nhau bằng cái mã khóa GTK đó.

## III. KRACK là gì?

KRACK attack, viết đầy đủ là Key Reinstallation Attack, là một loại tấn công bảo mật nghiêm trọng được phát hiện vào năm 2017 bởi các nhà nghiên cứu bảo mật. Tấn công này nhắm vào giao thức WPA2 (Wi-Fi Protected Access 2), một phương pháp mã hóa mạng không dây được sử dụng rộng rãi để bảo vệ thông tin trao đổi giữa các thiết bị và điểm truy cập Wi-Fi. Mặc dù WPA2 đã được coi là tiêu chuẩn bảo mật cao nhất cho mạng Wi-Fi trước khi KRACK được tiết lộ, nhưng phát hiện này đã cho thấy kỹ thuật mã hóa này cũng có điểm yếu có thể bị khai thác.

Android và Linux là 2 nền tảng ghi nhận những công kích đầu tiên từ lỗ hổng bảo mật Wi-Fi KRACK. Nguyên nhân là do các công ty này tuân thủ rất đúng thiết kế bảo mật 802.11x.

Windows, Mac OS và iOS lúc này vẫn đang an toàn, tuy nhiên thời gian "sung sướng" là không lâu, và hacker sẽ bắt đầu tấn công khi phân tích thành công tài liệu về 10 lỗi bảo mật đang bị rò rỉ ra thế giới bên ngoài.

Tuy vậy, may mắn là lỗi bảo mật này hầu hết đều có thể vá từ phía client (laptop, điện thoại) của người dùng mà không cần bắt buộc can thiệp vào Router Wi-Fi, chỉ cần vá 1 chiều là khả năng tấn công về gần như về "không".

Tuy nhiên, với lợi thế về nền tảng thì các hệ điều hành như Windows, iOS, MacOS rất dễ dàng ngăn cản các cuộc công kích bằng bản vá lỗi (Windows đã vá thành công).

Linux và Android, đặc biệt là trên các thiết bị đời cũ thì khả năng "sống chung với lũ" là rất cao. Vì bản vá lỗi sẽ ảnh hưởng rất nhiều đến quá trình hoạt động của thiết bị.

Hiện tại có 10 lỗi liên quan đến lổ hổng bảo mật này, và hacker có đến hàng trăm, hàng ngàn cách tấn công và khai thác khác nhau:

+ CVE-2017-13077: Reinstallation of the pairwise encryption key (PTK-TK) in the 4-way handshake.

+ CVE-2017-13078: Reinstallation of the group key (GTK) in the 4-way handshake.

+ CVE-2017-13079: Reinstallation of the integrity group key (IGTK) in the 4-way handshake.

+ CVE-2017-13080: Reinstallation of the group key (GTK) in the group key handshake.

+ CVE-2017-13081: Reinstallation of the integrity group key (IGTK) in the group key handshake.

+ CVE-2017-13082: Accepting a retransmitted Fast BSS Transition (FT) Reassociation Request and reinstalling the pairwise encryption key (PTK-TK) while processing it.

+ CVE-2017-13084: Reinstallation of the STK key in the PeerKey handshake.

+ CVE-2017-13086: reinstallation of the Tunneled Direct-Link Setup (TDLS) PeerKey (TPK) key in the TDLS handshake.

+ CVE-2017-13087: reinstallation of the group key (GTK) when processing a Wireless Network Management (WNM) Sleep Mode Response frame.

+ CVE-2017-13088: reinstallation of the integrity group key (IGTK) when processing a Wireless Network Management (WNM) Sleep Mode Response frame.

## IV. KRACK attack hoạt động như thế nào?

KRACK attack lợi dụng vào điểm yếu trong quy trình bắt tay 4 bước của cơ chế bảo mật WPA/WPA2:

Bước 1: thiết bị muốn truy cập WiFi (ví dụ như điện thoại, có thể gọi là Client) khi muốn truy cập tới router WiFi (có thể gọi là AP - Access Point) sẽ dò mạng và thấy sóng của router. Trong sóng phát thăm dò của router có mã ngẫu nhiên gọi là ANONCE, và điện thoại sẽ nhận lấy mã ANONCE.

Bước 2: điện thoại lấy mã ANONCE rồi tính toán ra một mã ngẫu nhiên khác gọi là SNONCE và gửi cho router kèm một số thông tin được mã hóa kèm SNONCE về danh tính và cả mật khẩu Wi-Fi.

Bước 3: router nhận được SNONCE thì sẽ biết được điện thoại gửi mật khẩu Wi-Fi đúng, từ đó router "hăm hở" gửi lại cho điện thoại mã khóa chung gọi là GTK (Group Temporal Key) để điện thoại dùng mã khóa này khi gửi thông tin cho router. Khi nhận được router sẽ biết mà giải mã.

Bước 4: điện thoại nhận được GTK sẽ lưu lại (Installation) rồi mã hóa một tín hiệu ACK gửi lại cho router để báo hiệu đã nhận được khóa. Rồi từ đó 2 phía nói với nhau bằng cái mã khóa GTK đó.

Bình thường cơ chế này an toàn vì điện thoại nếu không nhận được mã khóa chung GTK ở bước 3 thì không có dữ liệu quan trọng gì được chuyển đi tiếp nữa cả, kết nối bị mất. Nhưng rồi lỗi xảy ra ở bước 3 khi có đối tượng hacker chen vào giữa bước 3 và 4, lúc đó router gửi mã GTK quan trọng cho điện thoại nhưng hacker đã có thể "chôm" mã GTK và giấu đi. Và bình thường nếu giấu đi và điện thoại không nhận được GTK thì sẽ không có khóa để mã hóa dữ liệu ACK gửi đi nên coi như GTK không còn tác dụng gì. Nhưng điểm yếu bị phát hiện là khi router không thấy điện thoại nhận được GTK, sau một khoảng thời gian không thấy điện thoại phản hồi, thì lại gửi lại một cái GTK y chang như cái cũ. Vì thế đáng lễ khóa mã hóa chỉ được dùng bởi chỉ một mình chiếc điện thoại nhưng bây giờ có tới 2 đầu mối có thể cùng dùng khóa trong cùng lúc, đó là chiếc điện thoại của chúng ta và hacker. Nhờ vậy hacker có thể giải mã mọi dữ liệu gửi qua lại.

Ta có thể xem qua demo cho KRACK attack như sau:

Đầu tiên ta có 1 con network sử dụng WPA/WPA2:

![image](https://github.com/NVex0/An_Toan_Thuong_Mai_Dien_Tu/assets/113530029/f76404cc-c663-4965-beb4-3f68ab962b78)

Ta truy cập thử vào trang web. Web này sử dụng https:

![image](https://github.com/NVex0/An_Toan_Thuong_Mai_Dien_Tu/assets/113530029/47932d46-88cf-4ac3-ae88-d6d0a3fce029)

![image](https://github.com/NVex0/An_Toan_Thuong_Mai_Dien_Tu/assets/113530029/ba78ea3d-1dc8-4e97-94ce-e144bc0ea807)

Chạy PoC KRACK attack https://github.com/vanhoefm/krackattacks-scripts, truyền các param tương ứng card mạng và wifi name ta muốn tấn công:

https://github.com/vanhoefm/krackattacks-scripts

Trước hết, nó detect xem có wifi đó trong network không, ở đây là báo tìm thấy:

![image](https://github.com/NVex0/An_Toan_Thuong_Mai_Dien_Tu/assets/113530029/c48432bd-a2f0-4109-8783-42a202451851)

Sau khi tìm thấy, nó sẽ clone wifi này thành 1 rogue wifi trên 1 channel khác:

![image](https://github.com/NVex0/An_Toan_Thuong_Mai_Dien_Tu/assets/113530029/104051bb-5f0e-42ea-bd78-fb23e65ad065)

Sang máy điện thoại và connect vào wifi:

![image](https://github.com/NVex0/An_Toan_Thuong_Mai_Dien_Tu/assets/113530029/3fc3ff0c-b54f-48ea-b70a-a5fb0f7c200e)

Khi này, máy sẽ cố gắng connect vào con wifi thật kia, tuy nhiên PoC này được build để cố trick nó connect sang 1 channel khác - vào bản clone của wifi kia (rogue wifi), điều này nhằm tăng tỉ lệ thành công cho cuộc tấn công:

![image](https://github.com/NVex0/An_Toan_Thuong_Mai_Dien_Tu/assets/113530029/8d66d8cb-d40b-4ce1-a8ce-260b7f75e1cf)

Khi đã trick được nó connect vào rogue wifi, bắt đầu thực hiện KRACK lên quá trình bắt tay 4 bước:


