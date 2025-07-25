<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="utf-8">
  <title>LawTech Showcase</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      background: none;
      position: relative;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      color: white;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
      overflow-x: hidden;
    }

    #video-background {
  position: fixed;
  top: 0;
  left: 0;
  min-width: 100vw;
  min-height: 100vh;
  width: auto;
  height: auto;
  object-fit: cover;
  z-index: -1;
}

    .menu {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
      margin: 20px 0;
      width: 100%;
      max-width: 500px;
      padding: 0 10px;
      box-sizing: border-box;
    }

    .menu button {
      width: 100%;
      font-size: 1.1em;
      padding: 15px 10px;
      background-color: #222;
      color: #fff;
      border: 2px solid #4CAF50;
      border-radius: 12px;
      cursor: pointer;
      transition: transform 0.2s, background-color 0.3s;
      box-sizing: border-box;
    }

    .menu button:hover {
      background-color: #4CAF50;
      transform: scale(1.05);
    }

    .content {
      display: none;
      max-width: 800px;
      margin-top: 30px;
      padding: 20px;
      background-color: #222;
      border-radius: 10px;
      width: 90%;
      box-sizing: border-box;
    }

    .content.active {
      display: block;
    }

    .animated-title {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      padding: 10px;
    }

    .animated-title h1, .animated-title h2 {
      animation: fadeInUp 1s ease-out both;
      color: #FFD700;
      margin: 10px 0;
    }

    .animated-title img {
      max-width: 150px;
      height: auto;
      margin: 10px 0;
      display: block;
    }

    .glow {
      animation: glowAnim 2s infinite alternate;
    }

    @keyframes glowAnim {
      0% {
        text-shadow: 0 0 5px #FFD700, 0 0 10px #FFD700;
      }
      100% {
        text-shadow: 0 0 10px #FFD700, 0 0 20px #FFD700;
      }
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes marquee {
      0% { transform: translateX(100%); }
      100% { transform: translateX(-100%); }
    }

    @media screen and (max-width: 768px) {
      .menu {
        flex-direction: column;
        padding: 0 10px;
        gap: 12px;
      }

      .menu button {
        font-size: 1em;
        padding: 15px;
      }

      .animated-title h1,
      .animated-title h2 {
        font-size: 1.2em;
      }

      .animated-title img {
        width: 120px;
      }

      .content {
        width: 100%;
        padding: 15px;
      }

      video {
        width: 100% !important;
        height: auto !important;
      }
    }
  </style>
</head>

<body>

  <video id="video-background" autoplay loop muted>
    <source src="videonen2.mp4" type="video/mp4">
  </video>

  <div class="animated-title" style="background-color: rgba(0,0,0,0.6); padding: 30px 20px; margin: 30px auto; border-radius: 15px; max-width: 900px; box-shadow: 0 0 10px rgba(0,0,0,0.5);">
    <img src="logobca.png" alt="Logo Bộ Công an" style="height: 150px;">
    <h1 class="glow">PHẦN MỀM TRÌNH CHIẾU TƯƠNG TÁC</h1>
    <h1 class="glow">BÀI DỰ THI</h1>
    <h2>"TÌM HIỂU LUẬT DỮ LIỆU TRONG CÔNG AN NHÂN DÂN"</h2>
  </div>

  <div style="margin-bottom: 20px; width: 100%; overflow: hidden; background: rgba(0,0,0,0.6); padding: 10px 0;">
    <div class="marquee-text" style="display: inline-block; white-space: nowrap; animation: marquee 20s linear infinite; font-size: 1.1em; color: #FFD700;">
      📢 Luật dữ liệu trong thời kỳ chuyển đổi số quốc gia - Bước đột phá trong Kỷ nguyên mới - Kỷ nguyên vươn mình của Dân tộc 📢
    </div>
  </div>

  <div class="info-box" style="background-color: rgba(0,0,0,0.6); padding: 20px; margin: 20px auto 10px auto; border-radius: 10px; text-align: center; max-width: 1000px;">
    <p><span style="color: #FFD700;">Nhóm Tác giả:</span> <strong style="color: #FFD700;">CHIẾN BINH VIỄN THÔNG</strong></p>
    <p><span style="color: #FFD700;">Thành viên:</span> <strong style="color: #FFD700;">Thiếu tá Mai Hồ Trung Trinh - Thiếu úy Huỳnh Văn Tài</strong></p>
    <p><span style="color: #FFD700;">Đơn vị:</span> <strong style="color: #FFD700;">Phòng Thông tin liên lạc miền Nam - Cục H04 - Bộ Công an</strong></p>
  </div>

  <div class="menu">
    <button onclick="window.location.href='gioithieuchung.html'">📄  Thuyết minh bài dự thi</button>
    <button onclick="window.location.href='traloicauhoi.html'">📌 Trả lời câu hỏi bài dự thi</button>
    <button onclick="window.location.href='vanbanluat.html'">📚 Các văn bản Luật liên quan</button>
    <button onclick="showContent('tinhhuong')">🎥 Tình huống thực tiễn</button>
    <button onclick="showContent('tracnghiem')">🛡️ Trắc nghiệm khách quan</button>
    <button onclick="showContent('maQR')">🧠 Mã QR tài liệu</button>
    <button onclick="showContent('khuyennghi')">📎 Khuyến nghị</button>
  </div>

  <!-- Nội dung các phần -->
  <div id="traloicauhoi" class="content">
    <h2> Trả lời câu hỏi bài dự thi</h2>
    <ul>
      <li>Dữ liệu KH&CN là mục tiêu tấn công và đánh cắp.</li>
      <li>Rò rỉ dữ liệu có thể ảnh hưởng nghiêm trọng đến an ninh và công nghệ.</li>
      <li>Cần nắm vững luật bảo vệ dữ liệu và sở hữu trí tuệ.</li>
    </ul>
  </div>

  <div id="luat" class="content">
    <h2>Các văn bản luật liên quan</h2>
    <ul>
      <li>Nghị định 13/2023/NĐ-CP</li>
      <li>Luật An toàn thông tin mạng</li>
      <li>Luật Sở hữu trí tuệ (sửa đổi)</li>
      <li>Quy định bảo mật trong nghiên cứu quốc phòng</li>
    </ul>
  </div>

  <div id="tinhhuong" class="content" style="max-height: 500px; overflow-y: auto;">
    <h2>Video minh họa vi phạm dữ liệu KH&CN</h2>
    <p>1. Viện nghiên cứu bị tấn công mạng, rò rỉ dữ liệu AI quốc phòng.</p>
    <video controls style="width: 480px; height: 270px; border: 2px solid #444; border-radius: 8px;">
      <source src="onmt.mp4" type="video/mp4">
    </video>
    <p>2. Video về triển khai luật dữ liệu trong Công an nhân dân.</p>
    <video controls style="width: 480px; height: 270px; border: 2px solid #444; border-radius: 8px;">
      <source src="nen1.mp4" type="video/mp4">
    </video>
  </div>

  <div id="baove" class="content">
    <h2>Hướng dẫn bảo vệ dữ liệu KH&CN</h2>
    <ul>
      <li>Mã hóa dữ liệu</li>
      <li>Phân quyền truy cập</li>
      <li>Sao lưu định kỳ</li>
      <li>Không chia sẻ công khai</li>
      <li>Xác thực đa yếu tố</li>
    </ul>
  </div>

  <div id="tracnghiem" class="content">
    <h2>Trắc nghiệm khách quan</h2>
    <p>1. Luật nào bảo vệ dữ liệu cá nhân tại VN?</p>
    <p>☐ Luật Giao thông</p>
    <p>☑ Nghị định 13/2023/NĐ-CP</p>
    <p>2. Chia sẻ dữ liệu nghiên cứu trái phép vi phạm gì?</p>
    <p>☑ Luật Sở hữu trí tuệ</p>
    <p>☐ Luật Xây dựng</p>
  </div>

  <div id="maQR" class="content">
    <p><a href="files/LawTech_Showcase_Final.pptx" target="_blank" style="color: #4CAF50; text-decoration: underline;">📥 Tải bài trình chiếu PowerPoint tại đây</a></p>
    <img src="img/qrcode_tai_lieu.png" style="width: 150px;">
  </div>

  <div id="khuyennghi" class="content">
    <h2> Khuyến nghị</h2>
    <p>Nhóm Chiến Binh Viễn Thông<br>Phòng Thông tin Liên lạc Miền Nam</p>
    <p><em>Đồng hành cùng cuộc thi Tìm hiểu Luật Dữ liệu</em></p>
  </div>

  <script>
    function showContent(id) {
      document.querySelectorAll('.content').forEach(el => el.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }
  </script>

</body>
</html>
