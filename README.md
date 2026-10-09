Bài 3 stage 6

I, Sơ đồ IPO

1.Input: Tên thư mục, tên 3 file, nguồn code và đích sao lưu
   
2. Process: Tạo cây thư mục → tạo file → ẩn .env → sao chép code đệ quy
   
3. Output: smart-farm có code, data\logs và backup\code_v1

II,

1. Tạo cây thư mục lồng nhau `smart-farm\data\logs` và `smart-farm\code` chỉ bằng **duy nhất 1 dòng lệnh** PowerShell.

 New-Item -ItemType Directory -Force -Path "smart-farm\data\logs", "smart-farm\code", "smart-farm\backup"

2. Tạo cùng lúc 3 file cấu hình: `config.json`, `sensors.py`, `.env` (file ẩn) bằng **1 dòng lệnh** PowerShell.

 New-Item -ItemType File -Path "smart-farm\code\config.json", "smart-farm\code\sensors.py", "smart-farm\code\.env" 

3.  Sao chép toàn bộ thư mục `code` sang `backup\code_v1` (bao gồm cả nội dung bên trong).

  Copy-Item -Path "smart-farm\code" -Destination "smart-farm\backup\code_v1" -Recurse
   
