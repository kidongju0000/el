<html lang="en-US">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>달력 표</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }
        
        .top-link {
            display: block;
            padding: 12px 20px;
            background-color: #4CAF50;
            color: white;
            text-decoration: none;
            text-align: center;
            font-weight: bold;
            border-radius: 5px;
            margin-bottom: 20px;
            width: 100%;
            max-width: 500px;
        }
        
        .calendar-container {
            width: 100%;
            max-width: 500px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        .calendar-header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 15px;
            font-size: 1.2em;
        }
        
        .calendar {
            width: 100%;
            aspect-ratio: 1/1; /* 1:1 비율 유지 */
            border-collapse: collapse;
        }
        
        .calendar th {
            background-color: #f0f0f0;
            padding: 10px;
            text-align: center;
            color: #333;
        }
        
        .calendar td {
            padding: 12px;
            text-align: center;
            border: 1px solid #e0e0e0;
            cursor: pointer;
        }
        
        .calendar td:hover {
            background-color: #f0f0f0;
        }
        
        .current-day {
            background-color: #4CAF50;
            color: white;
            border-radius: 50%;
            display: inline-block;
            width: 24px;
            height: 24px;
            line-height: 24px;
        }
    </style>
</head>
<body>
    <a href="https://www.schoolwebsite.com" class="top-link" target="_blank">홈</a>
    
    <div class="calendar-container">
        <div class="calendar-header">
            2023년 11월
        </div>
        <table class="calendar">
            <thead>
                <tr>
                    <th>일</th>
                    <th>월</th>
                    <th>화</th>
                    <th>수</th>
                    <th>목</th>
                    <th>금</th>
                    <th>토</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td></td>
                    <td></td>
                    <td></td>
                    <td>1일 <br> 짜장면 </td>
                    <td>2일 <br> </td>
                    <td>3일 <br> </td>
                    <td>4일 <br> </td>
                </tr>
                <tr>
                    <td>5일 <br> </td>
                    <td>6일 <br> </td>
                    <td>7일 <br> </td>
                    <td>8일 <br> </td>
                    <td>9일 <br> </td>
                    <td>10일 <br> </td>
                    <td>11일 <br> </td>
                </tr>
                <tr>
                    <td>12일 <br> </td>
                    <td>13일 <br> </td>
                    <td>14일 <br> </td>
                    <td>15일 <br> </td>
                    <td>16일 <br> </td>
                    <td>17일 <br> </td>
                    <td>18일 <br> </td>
                </tr>
                <tr>
                    <td>19일 <br> </td>
                    <td>20일 <br> </td>
                    <td>21일 <br> </td>
                    <td>22일 <br> </td>
                    <td>23일 <br> </td>
                    <td>24일 <br> </td>
                    <td>25일 <br> </td>
                </tr>
                <tr>
                    <td>26일 <br> </td>
                    <td>27일 <br> </td>
                    <td>28일 <br> </td>
                    <td>29일 <br> </td>
                    <td>30일 <br> </td>
                    <td></td>
                    <td></td>
                </tr>
            </tbody>
        </table>
    </div>

    <script>
        // 현재 날짜 표시 기능
        document.addEventListener('DOMContentLoaded', function() {
            const today = new Date();
            const currentDate = today.getDate();
            const currentMonth = today.getMonth() + 1;
            const currentYear = today.getFullYear();
            
            // 현재 월 표시
            if(currentMonth === 11 && currentYear === 2023) {
                const cells = document.querySelectorAll('.calendar td');
                cells.forEach(cell => {
                    if(cell.textContent == currentDate) {
                        cell.innerHTML = `<span class="current-day">${currentDate}</span>`;
                    }
                });
            }
        });
    </script>
</body>
</html>
