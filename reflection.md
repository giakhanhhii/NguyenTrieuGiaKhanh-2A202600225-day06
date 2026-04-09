# **Individual reflection \- Nguyễn Triệu Gia Khánh \- 2A202600225**

## **1\. Role**

**AI Engineer \+ Data Engineer.** Phụ trách xây dựng lõi logic cho AI Agent (Loop) và hệ thống thu thập dữ liệu (Crawl tool).

## **2\. Đóng góp cụ thể**

* **Xây dựng AI Agent Loop:** Thiết kế và triển khai luồng lặp cho Agent 1 & Agent 2, xử lý các lỗi logic (fix bug agent1.py, agent2.py) để đảm bảo hệ thống phản hồi ổn định.  
* **Data Acquisition:** Phát triển công cụ crawl dữ liệu bác sĩ từ Vinmec (crawl\_vinmec\_doctor.py), cung cấp tập dữ liệu đầu vào chuẩn cho hệ thống gợi ý.  
* **Hỗ trợ Backend:** Phối hợp cùng team refactor lại các file trong folder app/ và services/ để tích hợp AI Agent vào luồng xử lý chung.

## **3\. SPEC mạnh/yếu**

* **Mạnh nhất (Technical Logic):** Hệ thống xử lý được các vòng lặp phản hồi của Agent, đảm bảo khi thông tin thiếu, AI biết cách truy vấn lại hoặc tìm kiếm thêm từ dữ liệu đã crawl thay vì trả lời sai.  
* **Yếu nhất (Data Diversity):** Do giới hạn thời gian, công cụ crawl mới chỉ tập trung tối ưu cho một nguồn dữ liệu nhất định. Nếu mở rộng ra nhiều hệ thống bệnh viện khác nhau, cần xử lý thêm các vấn đề về cấu trúc dữ liệu không đồng nhất.

## **4\. Đóng góp khác**

* Hỗ trợ team debug các lỗi liên quan đến kết nối giữa AI Service và Backend Server.  
* Tối ưu hóa các prompt nội bộ trong Agent Loop để giảm latency (độ trễ) khi phản hồi người dùng.

## **5\. Điều học được**

Qua dự án này, mình nhận ra rằng việc xây dựng một AI Agent không chỉ là viết prompt hay gọi API, mà quan trọng nhất là thiết kế **Loop logic**. Việc xử lý dữ liệu thực tế (Real-world data) từ công cụ crawl giúp mình hiểu rõ hơn về tầm quan trọng của việc làm sạch dữ liệu trước khi đưa vào mô hình ngôn ngữ lớn (LLM).

## **6\. Nếu làm lại**

Mình sẽ ưu tiên việc triển khai hệ thống **Vector Database** sớm hơn ngay từ ngày đầu tiên thay vì chỉ lưu trữ dữ liệu crawl thô. Điều này sẽ giúp các Agent truy xuất thông tin bác sĩ và chuyên khoa với độ chính xác và tốc độ cao hơn nữa.

## **7\. AI giúp gì / AI sai gì**

* **Giúp:** Sử dụng AI để viết nhanh các đoạn script boilerplate cho công cụ crawl và gợi ý các hướng xử lý lỗi logic trong Python nhanh chóng.  
* **Sai/mislead:** Đôi khi AI gợi ý các cấu trúc code quá phức tạp hoặc sử dụng các thư viện không cần thiết cho quy mô hackathon, dễ dẫn đến lãng phí thời gian nếu không tỉnh táo sàng lọc.

