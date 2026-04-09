# local-ai-assistant
an AI assistant that run on your local machine :)

Instruction:

Step 1: 
- Download model tại: https://huggingface.co/Qwen/Qwen2.5-1.5B-Instruct-GGUF/tree/main
- Tại ổ C , tạo một thư mục là MyLocalAI, copy model AI vào thư mục này, giải nén zip vào trong thư mục MyLocalAI.

Step 2: Mở CMD tại đường dẫn MyLocalAI, chạy lệnh sau :

llama-server.exe -m qwen2.5-1.5b-instruct-q2_k.gguf --port 8080 --host 127.0.0.1

-m: Tên file model của bạn.

--port 8080: Cổng mà web sẽ gọi vào.

--host 127.0.0.1: Chỉ chạy nội bộ trên máy bạn (Offline).

Khi nào hiện now listening on ... là đã thành công.

Step 3: Đảm bảo rằng index.html trong đó JS phần fetch trỏ đúng địa chỉ http://127.0.0.1:8080/v1/chat/completions

Mở bằng Chrome, nhập và ấn gửi.

Lưu ý:

- Windows only
- Lỗi CORS: nếu bị lỗi này thì hãy thêm lệnh --embedding --cors vào sau lệnh ở Step 2