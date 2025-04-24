# etl-mavenfuzzy
Sau khi thực hiện file createmavenfuzzyfactory.sql sẽ nhận được các bảng cũng như data của nó như hình sau : 
![image](https://github.com/user-attachments/assets/6511b8b6-38a2-4078-bf42-6a818e1a2a4e)
Dựa trên dữ liệu đã cho, em sẽ tạo các bảng như dim_channel, dim_date, dim_produc, dim_device, dim_page,..
Và các bảng fact_sales, face_website_activity cũng như các tranform để tạo bảng agg_daily_sales và agg_daily_webtraffic như sau 
![image](https://github.com/user-attachments/assets/05a4c684-5618-4e2e-9042-280c17647333)

## Dưới đây là dữ liệu mẫu của một số bảng 
![image](https://github.com/user-attachments/assets/1b65e0f1-597e-48f5-9e82-53c8616a57ab)
![image](https://github.com/user-attachments/assets/f6786605-fe29-4088-88b1-32632527c227)
![image](https://github.com/user-attachments/assets/86378f5e-d9a1-4369-bc5e-fe0f10f86461)
## Sau đó mình sẽ đi xây dựng một datapile với airflow và postgresql, dbt

![etl pic](https://github.com/user-attachments/assets/a90c5d80-27b5-4edb-a6d6-1ca156a0adc3)
Sau khi chạy dags thì các dữ liệu cơ bản và dữ liệu từ các bảng dim đã được chuyển vào trong postgresql
ví dụ như dim_page được chạy ở đây 
![image](https://github.com/user-attachments/assets/8ae0cc0b-dc5c-446d-829f-40b800855ff0)
và dim_product
![image](https://github.com/user-attachments/assets/0f564ea3-3573-4813-8f2e-9e2ea66738d8)

## Các bước thực hiện ETL 
Load data from creatmavenfuzzyfactory.sql bằng sql
Setup airflow, dags và env để thực hiện transform dữ liệu đã load được vào postgresql
Sơ đồ etl dự kiến 
![image](https://github.com/user-attachments/assets/9e6a7260-6a2c-4dac-9dc5-a8ee97bfdff0)


## Tiếp theo là thực hiện một số truy vấn nâng cao 
# Đầu tiên là tổng doanh thu cho từng sản phẩm
![image](https://github.com/user-attachments/assets/1abaf107-b581-48a2-8fd7-87889ed3d809)
# Tiếp theo là tỉ lệ chuyển đổi cho từng kênh
![image](https://github.com/user-attachments/assets/beea33a0-c00e-416c-83aa-ea3e7bddca95)

# Và các thông số của từng năm 
![image](https://github.com/user-attachments/assets/916225e4-a6ba-4cc0-90dd-a8e4596d84e8)

# Tiếp theo là thông số của từng tháng
![image](https://github.com/user-attachments/assets/6b72c54e-6c07-49dc-b74a-358f2ed84c9b)

# Thông số của từng quý 
![image](https://github.com/user-attachments/assets/8b86c2dc-30a9-4eea-8052-b7dd6a88ea35)

# So sánh giữa các quý trong 2 năm liêp tiếp 
![image](https://github.com/user-attachments/assets/bea99f6b-fe5e-4762-a6dd-a582011952d4)

# Và cuối cùng là thông số các kênh tiếp thị theo các quý 
![image](https://github.com/user-attachments/assets/5bdeb329-3f79-4796-91be-5f0cb1ce22dc)





