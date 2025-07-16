# Multiview_IL

## Giới thiệu

`Multiview_IL` là một codebase về học tăng cường độc lập đa quan sát (Multi-view Imitation Learning) sử dụng trên nền tảng mô phỏng lái xe [CARLA](https://carla.org/). Dự án này tích hợp nhiều thành phần bao gồm định nghĩa kịch bản giao thông, engine thực thi mô phỏng, các agent tự động hóa, và các công cụ giải thích mô hình học sâu.

## Tính năng chính

- **Định nghĩa và thực thi kịch bản giao thông cho CARLA** (thư mục `scenario_runner`)
    - Hỗ trợ chuẩn [OpenSCENARIO](http://www.openscenario.org/) cho mô tả kịch bản mô phỏng
    - Có thể sử dụng để huấn luyện, kiểm thử agent cho thử thách [CARLA Challenge](https://carla-challenge.org/)
- **Triển khai agent tự lái học tăng cường đa quan sát** (thư mục `run_CARLA_driving`)
    - Agent kế thừa chuẩn của CARLA, có thể xử lý dữ liệu hình ảnh, tốc độ, GPS, IMU, v.v.
    - Hỗ trợ ghi nhận dữ liệu quá trình lái, xử lý tín hiệu điều khiển (steer, throttle, brake)
- **Công cụ giải thích mô hình deep learning** (`pytorch_grad_cam`)
    - Hỗ trợ các phương pháp Class Activation Map (CAM) cho cả Classification, Object Detection, Semantic Segmentation
    - Hỗ trợ các kiến trúc CNN, Vision Transformer, Swin Transformer, YOLO, Faster-RCNN, v.v.

## Yêu cầu hệ thống

- **Python**: Tương thích Python 2.7, 3.5, 3.6 (ưu tiên Python 3.x)
- **CARLA Simulator**: Tải và cài đặt theo hướng dẫn tại [carla.org](https://carla.org/)
- **Các thư viện phụ thuộc**: (xem chi tiết trong từng thư mục, ví dụ như requirements.txt hoặc README.md các module con)
    - `autopep8`, `pylint`, `numpy`, `torch`, `plotly`, v.v.

## Hướng dẫn cài đặt nhanh

1. Clone repo:
    ```bash
    git clone https://github.com/anhht9824/Multiview_IL.git
    ```

2. Cài đặt các phụ thuộc Python (giả sử dùng Python 3):
    ```bash
    pip install -r requirements.txt
    ```

3. Cài đặt và khởi động CARLA Simulator theo hướng dẫn chính thức.

4. Chạy thử kịch bản mẫu hoặc agent:
    - Xem hướng dẫn chi tiết trong `scenario_runner/README.md` và `run_CARLA_driving/README.md`

## Coding Standard

- Mã Python tuân thủ PEP8, sử dụng `autopep8` để format, kiểm tra với `pylint`
- Hạn chế cảnh báo/ lỗi khi compile/run code (C++ dùng chuẩn Google Style Guide, Unreal Engine Coding Standard)

## Đóng góp

- Vui lòng đọc `scenario_runner/Docs/CONTRIBUTING.md` và `CODE_OF_CONDUCT.md`
- Luôn kiểm tra issue board trước khi bắt đầu.
- Pull request cần mô tả rõ ràng, kèm hình ảnh/ GIF minh họa nếu có.

## Giấy phép

MIT License.

---

> Xem thêm chi tiết trong từng thư mục:  
> - `scenario_runner/README.md`: Hướng dẫn về kịch bản mô phỏng  
> - `run_CARLA_driving/pytorch_grad_cam/README.md`: Hướng dẫn sử dụng Grad-CAM  
> - Tài liệu đóng góp: `scenario_runner/Docs/CONTRIBUTING.md`
