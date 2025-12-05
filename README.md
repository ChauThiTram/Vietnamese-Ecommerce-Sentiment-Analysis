
# Vietnamese Sentiment Analysis with PhoBERT

## Giới thiệu
Dự án xây dựng mô hình phân loại cảm xúc bình luận cho các sàn thương mại điện tử tại Việt Nam. Mô hình phân loại bình luận thành 3 nhãn: **Tích cực (Positive), Tiêu cực (Negative), Trung lập (Neutral)**.

Điểm đặc biệt: Dự án sử dụng kỹ thuật **Data Augmentation** bằng **Google Gemini API** để xử lý vấn đề mất cân bằng dữ liệu.

## Mô hình và Kỹ thuật
* **Model:** Fine-tuning mô hình **PhoBERT** (`vinai/phobert-base`).
* **Thư viện:** PyTorch, HuggingFace Transformers, Scikit-learn.
* **Xử lý dữ liệu:**
    * Chuẩn hóa văn bản (Normalize Text), xử lý teencode.
    * Sinh dữ liệu nhân tạo (Synthetic Data Generation) với Gemini API.

## Kết quả (Performance)
* **Accuracy:** ~78% (trên tập test).
* Có tích hợp module đánh giá sai số (Error Analysis) tự động.

## Dữ liệu
* File `sample_data.csv`: Chứa mẫu dữ liệu demo (Do dataset gốc khá nặng nên không upload lên đây).
* Cấu trúc dữ liệu gồm 2 cột: `comment` (nội dung) và `label` (nhãn).

## Cách sử dụng (Notebook)
Mở file `Sentiment_Analysis_PhoBERT.ipynb` trên Google Colab hoặc Jupyter Notebook để xem toàn bộ quy trình từ xử lý dữ liệu đến huấn luyện và đánh giá.
