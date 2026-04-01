# METC-shuttle-table-for-support-team
METC shuttle table for support team
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>搭車登記系統</title>
    <style>
        body { font-family: -apple-system, "Helvetica Neue", sans-serif; background-color: #f4f7f9; display: flex; justify-content: center; padding: 20px; }
        .form-container { background: white; padding: 30px; border-radius: 12px; box-shadow: 0 4px 20px rgba(0,0,0,0.08); width: 100%; max-width: 500px; }
        h2 { color: #333; text-align: center; margin-bottom: 25px; }
        .form-group { margin-bottom: 18px; }
        label { display: block; margin-bottom: 8px; font-weight: 600; color: #555; }
        input, select { width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 6px; box-sizing: border-box; font-size: 16px; }
        .time-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
        button { width: 100%; padding: 14px; background-color: #007AFF; color: white; border: none; border-radius: 6px; font-size: 18px; cursor: pointer; margin-top: 20px; transition: background 0.3s; }
        button:hover { background-color: #0056b3; }
    </style>
</head>
<body>

<div class="form-container">
    <h2>接駁車搭乘登記</h2>
    <form id="shuttleForm">
        <div class="form-group">
            <label for="name">登記名字</label>
            <input type="text" id="name" name="name" placeholder="請輸入姓名" required>
        </div>

        <div class="time-grid">
            <div class="form-group">
                <label for="arrivalDate">抵達日期</label>
                <input type="date" id="arrivalDate" name="arrivalDate" required>
            </div>
            <div class="form-group">
                <label for="returnDate">回程日期</label>
                <input type="date" id="returnDate" name="returnDate" required>
            </div>
        </div>

        <div class="time-grid">
            <div class="form-group">
                <label for="startTime">上班時間</label>
                <select id="startTime" name="startTime">
                    <option value="08:00">08:00</option>
                    <option value="08:30">08:30</option>
                    <option value="09:00">09:00</option>
                    <option value="其他">其他</option>
                </select>
            </div>
            <div class="form-group">
                <label for="endTime">下班時間</label>
                <select id="endTime" name="endTime">
                    <option value="17:00">17:00</option>
                    <option value="17:30">17:30</option>
                    <option value="18:00">18:00</option>
                    <option value="其他">其他</option>
                </select>
            </div>
        </div>

        <div class="form-group">
            <label for="hotel">酒店地點登記</label>
            <input type="text" id="hotel" name="hotel" placeholder="例如：曼谷大倉酒店" required>
        </div>

        <button type="submit">提交登記</button>
    </form>
</div>

<script>
    document.getElementById('shuttleForm').onsubmit = function(e) {
        e.preventDefault();
        alert('登記成功！已記錄您的搭車需求。');
        // 這裡可以串接 Google Sheets API 或後端資料庫
    };
</script>

</body>
</html>
