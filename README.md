<html></html>

<head>
<meta http-equiv="Content-Language" content="en-us">
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<title>Java script</title>
<script>
function Nhan()
{
	var a=document.getElementById("txtA").value;
	var b=document.getElementById("txtB").value;
	document.getElementById("txtKQ").value= a*b ;
}

function Chia()
{
	var a=document.getElementById("txtA1").value;
	var b=document.getElementById("txtB1").value;
	document.getElementById("txtKQ1").value= a/b ;
}

function Cong()
{
	var a=parseFloat(document.getElementById("txtA2").value);
	var b=parseFloat(document.getElementById("txtB2").value);
	document.getElementById("txtKQ2").value= a+b ;
}

function Tru()
{
	var a=parseFloat(document.getElementById("txtA3").value);
	var b=parseFloat(document.getElementById("txtB3").value);
	document.getElementById("txtKQ3").value= a-b ;
}

function giaiPhuongTrinh() {
        var a = parseFloat(document.getElementById("a").value);
        var b = parseFloat(document.getElementById("b").value);

        if (a == 0) {
            if (b == 0) {
                document.getElementById("ketQua").innerHTML = "Phương trình vô số nghiệm";
            } else {
                document.getElementById("ketQua").innerHTML = "Phương trình vô nghiệm";
            }
        } else {
            var x = -b / a;
            document.getElementById("ketQua").innerHTML = "Nghiệm của phương trình: x = " + x;
        }
    }

    function tinhSoNgay() {
        var thang = parseInt(document.getElementById("thang").value);
        var nam = parseInt(document.getElementById("nam").value);
        var soNgay;

        if (thang == 2) {
            if ((nam % 4 == 0 && nam % 100 != 0) || nam % 400 == 0) {
                soNgay = 29; // Năm nhuận
            } else {
                soNgay = 28;
            }
        } else if (thang == 4 || thang == 6 || thang == 9 || thang == 11) {
            soNgay = 30;
        } else {
            soNgay = 31;
        }

        document.getElementById("ketQua").innerHTML = "Số ngày trong tháng " + thang + " năm " + nam + " là: " + soNgay;
    }

</script>
</head>
<body>
<p>Java script</p>
<p>Tác dụng: làm trang web linh hoạt + có tương tác</p>
<p>Các phép toán cơ bản</p>

<p>Phép nhân:
<input type="text" id="txtA" name="T2" size="13">&nbsp; x&nbsp; 
<input type="text" id="txtB" name="T3" size="14">&nbsp;
<input type="button" value=" = " onclick="Nhan()" >
<input type="text" id="txtKQ" name="T6" size="16"> </p>

<p>Phép chia:
<input type="text" id="txtA1" name="T2" size="13">&nbsp; :&nbsp;
<input type="text" id="txtB1" name="T3" size="14">&nbsp;
<input type="button" value=" = " onclick="Chia()" >
<input type="text" id="txtKQ1" name="T6" size="16"> </p>

<p>Phép cộng: 
<input type="text" id="txtA2" name="T2" size="13">&nbsp; +&nbsp;
<input type="text" id="txtB2" name="T3" size="14">&nbsp;
<input type="button" value=" = " onclick="Cong()" >
<input type="text" id="txtKQ2" name="T6" size="16"> </p>

<p>Phép trừ: 
<input type="text" id="txtA3" name="T2" size="13">&nbsp; -&nbsp; 
<input type="text" id="txtB3" name="T3" size="14">&nbsp;
<input type="button" value=" = " onclick="Tru()" >
<input type="text" id="txtKQ3" name="T6" size="16"> </p>

<p>Giải phương trình bậc nhất: ax + b = 0</p>
<label for="a">Nhập số a:</label>
<input type="number" id="a">
<br><br>
<label for="b">Nhập số b:</label>
<input type="number" id="b">
<br><br>
<button onclick="giaiPhuongTrinh()">Giải phương trình</button>
<br><br>
<p id="ketQua"></p>

<p>Tính số ngày của một tháng khi biết tháng và năm</p>
<label for="thang">Nhập tháng:</label>
<input type="number" id="thang" min="1" max="12">
<br><br>
<label for="nam">Nhập năm:</label>
<input type="number" id="nam">
<br><br>
<button onclick="tinhSoNgay()">Tính số ngày</button>
<br><br>
<p id="ketQua"></p>


</body>
</html>
