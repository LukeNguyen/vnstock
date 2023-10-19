# Tài nguyên quan trọng

Trước khi bắt đầu, bạn có thể xem Video giới thiệu chính thức cho vnstock mình mới chia sẻ trên Youtube tại đây:

<iframe width="800" height="452" src="https://www.youtube.com/embed/6kP2TTtEY9Y?si=EOe0aW8cpqLyCnw5" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Website chính thức của vnstock

vnstock đã hoàn thiện bước đầu việc xây dựng một website chuyên biệt để cập nhật thông tin về dự án, tài liệu sử dụng, blog, khóa học, và các tài nguyên hữu ích khác. Các nội dung của website đang từng bước được cập nhật và hoàn thiện.

Bạn có thể truy cập [vnstock.site](https://vnstock.site?utm_source=vnstock-docs&utm_medium=resource) để biết thêm chi tiết.

Bạn cũng có thể truy cập vnstock Web app dưới đây được nhúng trên website của vnstock để người dùng tiện tìm và sử dụng.

## vnstock Web app
vnstock Web app đã được giới thiệu lần đầu vào 4/9/2023 nhằm giúp người dùng phổ thông có thể tiếp cận với vnstock theo cách đơn giản và thuận tiện nhất dù cho bạn không có bất cứ kỹ năng hay hiểu biết về lập trình python để sử dụng. 

vnstock web app được xây dựng bằng streamlit framework, sử dụng ngôn ngữ Python hoàn toàn. Đây  cũng là một định hướng rất triển vọng trong việc xây dựng các ứng dụng web trong việc phân tích chứng khoán với giao diện người dùng thân thiện và dễ sử dụng, bảo trì.

👉 Bạn có thể truy cập vnstock Web app để trải nghiệm ngay. 

[Mở Web App :material-rocket-launch:](https://vnstock.site/vnstock-app?utm_source=vnstock-docs&utm_medium=resource){ .md-button }

## Notebook minh hoạ
👉 Bạn có thể mở tệp Jupyter Notebook và dùng thử tất cả các hàm của vnstock từ giao diện Google Colab. Nếu muốn sử dụng Notebook trong Visual Studio Code hoặc IDE khác, bạn có thể tìm menu **File** > **Download** và chọn **Download.ipynb** để lưu file về máy.

[Mở Notebook :material-rocket-launch:](https://colab.research.google.com/github/thinh-vu/vnstock/blob/beta/docs/gen2_vnstock_demo_index_all_functions_testing_2023.ipynb){ .md-button }

## Docstring
Tất cả các hàm của vnstock đều được cung cấp docstring đầy đủ trong khi file README.md này có thể không cập nhật toàn bộ mô tả về các tham số cho phép của từng hàm. Bạn có thể xem phần gợi ý khi viết câu lệnh trên các IDE như Google Colab, Visual Studio Code, hay Jupyter Notebook hoặc mở phần source code của Github để xem chi tiết. Trong thời gian tới, vnstock sẽ được bổ sung mô tả đầy đủ tại README.md khi có thể.

- **Docstring trên Google Colab**: Gợi ý cú pháp hàm được hiển thị khi viết bất kỳ hàm nào thuộc vnstock, trong ví dụ này hiển thị trong giao diện Google Colab.

![docstring suggestion](../assets/images/docstring_suggestion.jpeg)

- **Docstring trong mã nguồn**: Mở mã nguồn Github tại thư mục vnstock, tìm hàm bạn cần tra cứu docstring.

![docstring source](../assets/images/docstring_source_code.png)

## vnstock cho Google Sheets
Tôi cung cấp một hàm tùy biến làm mẫu giúp bạn hình dung và bắt đầu tùy biến các hàm python được cung cấp bởi vnstock sang ngôn ngữ Google Apps Script và sử dụng để lấy dữ liệu trên Google Sheets. Bạn có thể bắt đầu đóng góp vào source code này giúp vnstock hoàn thiện đầy đủ các tính năng cho Google Sheets và lan tỏa tới cộng đồng.

- Để sử dụng thử đoạn code trên cho việc lấy dữ liệu, bạn làm như sau:
  - Mở file [source code vnstock_gg_sheet](https://github.com/thinh-vu/vnstock/blob/main/vnstock_gg_sheet/vnstock._appscript.js) và copy đoạn code.
  - Mở hoặc tạo 1 file Google Sheets bất kỳ
  - Từ menu của Google Sheets, tìm mục Extension (tiện ích mở rộng) > Apps Script như trong hình. 
  
![google sheets](../assets/images/google_sheet_appscript_menu.png)

  - Trong giao diện Apps Script Editor, xóa hết code hiện tại và ghi đè với đoạn code bạn copy từ source code ở trên 
  

- Mở rộng để xem ảnh minh họa trên Google Apps Script

![vnstock apps script](../assets/images/vnstock_google_sheets_appscript_code.png)
  
- Save file (Ctrl/Cmd + S) để lưu thay đổi.
- Chuyển qua Google Sheets, bạn đã có thể nhập các tham số cho hàm và sử dụng như bình thường. Ví dụ: `= derivativesOhlc("VN30F1M", "2023-06-01", "2023-09-26", "15")`
- Đây là kết quả bạn sẽ nhận được:

![vnstock sheets results](../assets/images/vnstock_google_sheet_result.png)

- Để chuyển đổi các hàm python hiện tại do vnstock cung cấp, bạn có thể sử dụng công cụ ChatGPT để thực hiện. Bạn sẽ cần có chút kiến thức về JavaScript để có thể tùy biến các hàm này nhanh chóng. Nếu không sẽ cần kỹ năng prompt engineering tốt để có thể yêu cầu AI hỗ trợ. Xa hơn, khi có nguồn lực, tôi sẽ cung cấp Add-in cho Google Sheets để các bạn có thể sử dụng dễ dàng hơn. Bạn có thể xem video hướng dẫn dưới đây để hiểu cách dùng ChatGPT hỗ trợ chuyển đổi hàm Python sang JavaScript.

<iframe width="800" height="452" src="https://www.youtube.com/embed/w4GCFZUpsEY?si=r77JMNc2p-SUihI5" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
