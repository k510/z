<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>表格计算结果</title>
    <script>
        function calculateRowTotal() {
            var table = document.getElementById('dataTable');
            var totalSum = 0;

            // 遍历表格中的每一行
            for (var i = 1; i < table.rows.length; i++) {
                // 获取第二列和第三列的值
                var value1 = parseFloat(table.rows[i].cells[1].getElementsByTagName('input')[0].value);
                var value2 = parseFloat(table.rows[i].cells[2].getElementsByTagName('input')[0].value);

                // 计算第四列的值（第二列乘以第三列）
                var result = value1 * value2;
                result = isNaN(result) ? 0 : result;

                // 将计算结果显示在第四列
                table.rows[i].cells[3].innerHTML = result;

                // 计算每行的总和并累加到总数中
                totalSum += result;
            }

            // 将结果显示在页面上
            document.getElementById('result').innerHTML = '总和是：' + totalSum;
        }
    </script>
</head>
<body>
    <table id="dataTable" border="1">
        <tr>
            <th>列1</th>
            <th>列2</th>
            <th>列3</th>
            <th>列4</th>
        </tr>
        <!-- 表格的行 -->
        <!-- 这里创建了21行，每一行包含两个输入框和一个只读的列 -->
        <!-- 用户可以在输入框中输入数字 -->
        <!-- 如果需要更多行，可以复制这些<tr>元素 -->
        <!-- 这里设置了一个简单的id来识别每个输入框 -->
        <!-- 这种设置并不是最佳实践，但对于这个简单示例来说是可以接受的 -->
        <!-- 如果您有更复杂的需求，需要更合适的id分配方式 -->
        <!-- 比如在后台动态生成表格时生成唯一的id -->
        <tr>
            <td>小花</td>
            <td><input id="num" type="number" value="5"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>鱼</td>
            <td><input id="num" type="number" value="220"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>魔女</td>
            <td><input id="num" type="number" value="10"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>锦鲤</td>
            <td><input id="num" type="number" value="10"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>大花</td>
            <td><input id="num" type="number" value="10"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>挚爱玫瑰</td>
            <td><input id="num" type="number" value="52"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>云迹寻梦</td>
            <td><input id="num" type="number" value="52"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>热气球</td>
            <td><input id="num" type="number" value="52"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>风铃</td>
            <td><input id="num" type="number" value="5"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>鲤鱼</td>
            <td><input id="num" type="number" value="10"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>龙</td>
            <td><input id="num" type="number" value="10"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>荧光棒</td>
            <td><input id="num" type="number" value="10"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>真爱玫瑰</td>
            <td><input id="num" type="number" value="99"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>告白信</td>
            <td><input id="num" type="number" value="52"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>狗粮</td>
            <td><input id="num" type="number" value="52"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>
        <tr>
            <td>戳戳</td>
            <td><input id="num" type="number" value="2"></td>
            <td><input type="text" oninput="calculateRowTotal()"></td>
            <td></td>
        </tr>


        <!-- 以此类推，直到21行 -->
    </table>
    <!-- 添加按钮用于计算结果 -->
    <button onclick="calculateResult()">计算结果</button>
    <!-- 显示计算结果 -->
    <div id="result"></div>
</body>
</html>
