# Câu 1
- Lỗi 1: Thao tác kiểm tra và thao tác lưu không được đảm bảo tính nguyên tử atomic. Khi người dùng click nhiều lền yêu cầu cấp lại đơn thuốc hoặc đơn dỉan hơn chuột bị double click hoặc hệ thống bị tấn công sẽ có thể xảy ra trường hợp nhiều luồng đọc được số cấp lại nhỏ hơn 0. Kết quả là đơn thuốc có thể bị lấy nhiều lần. Bệnh nhân sẽ lấy được số thuốc vượt chỉ định, hoặc có nguy cơ tích trữ thuốc
- Lỗi 2: Lỗi về bảo mật. Mã nguồn tìm kiếm thuốc sau đó lập bản cấp thuốc và gán ID bệnh nhân. Hệ thống không kiểm tra người gọi API có phải chủ cuar đơn thuốc hay không
# Câu 2
- Giải pháp 1: Không nên thục hiện các thao tác đọc, ghi trên application mà không có khóa. Dùng optimistic lock hoặc truy vấn  nguyên tử
- Giải pháp 2: Phải đối chiếu id bệnh nhân từ request với id bệnh nhân ở cơ sở dữ liệu của đơn thuốc trươccs khi sử lý
# Câu 3
Trong hệ thống y tế các lỗi trên bị đánh giá nghiêm trọng hơn so với các hệ thống khác vì mang nguy cơ ảnh hưởng đến sức khỏe bệnh nhân và có rủi ro pháp lý.