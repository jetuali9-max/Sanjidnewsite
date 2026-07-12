<!DOCTYPE html>
<html>
<head>
    <title>My Table</title>

    <style>
        table {
            border-collapse: collapse;
            width: 100%;
            text-align: center;
        }

        th, td {
            border: 1px solid black;
            width: 150px;
            height: 120px;
        }

        img {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
        }

        .form-box {
            margin-top: 20px;
            text-align: center;
        }

        input {
            padding: 8px;
            margin: 5px;
        }

        button {
            padding: 8px 15px;
            background: green;
            color: white;
            border: none;
            border-radius: 5px;
        }
    </style>

</head>
<body>

<h1><u>MC LIST</u></h1>

<table>
    <tr>
        <th>NAME</th>
        <th>PHOTO</th>
        <th>GF</th>
    </tr>

    <tr>
        <td><mark>ABDULLAH</mark></td>
        <td><img src="https://i.ibb.co.com/7N2DjBVf/IMG-20260414-160115-removebg-preview.png"></td>
        <td>(-1) guwa mara khwe che</td>
    </tr>

    <tr>
        <td><mark>HABIBUR</mark></td>
        <td><img src="https://i.ibb.co.com/s9RQL5sf/IMG-20260520-161759.jpg"></td>
        <td>AMI <i>LOCHHA MEYE DEKHLE 🤤</i></td>
    </tr>

    <tr>
        <td><mark>RAYHAN</mark></td>
        <td><img src="https://i.ibb.co.com/DH7ysM44/Screenshot-2026-07-13-01-25-25-962-com-zhiliaoapp-musically-edit.jpg"></td>
        <td>bibahito go jamawi 🫃</td>
    </tr>

    <!-- Inbox Row -->
    <tr>
        <td><a href="https://wa.me/8801628801587">Inbox</a></td>
        <td><a href="https://wa.me/8801628801587">Add New</a></td>
        <td><a href="https://wa.me/8801628801587">Send Info 📥</a></td>
    </tr>

</table>

<hr>

<!-- FORM -->
<div class="form-box">
    <h3>Add Yourself</h3>

    <input type="text" id="name" placeholder="Your Name"><br>
    <input type="number" id="number" placeholder="Your Number"><br>
    <input type="file"><br>

    <button onclick="sendToWhatsApp()">Send to Inbox</button>
</div>

<hr>

<!-- CONTACT -->
<p style="text-align:center; color:green;">
    <mark>jara number dichea tader contact number </mark>
</p>

<div style="text-align:center;">
    <a href="https://wa.me/8801827741059">📱 Abdullah</a><br><br>
    <a href="https://wa.me/8801880441162">📱 Habibur</a><br><br>
    <a href="https://wa.me/8801311708790">📱 Rayhan</a>
</div>

<!-- FOOTER -->
<footer style="background:black; text-align:center; padding:10px; margin-top:20px;">
    <p style="color:white;">© sanjid</p>
</footer>

<script>
function sendToWhatsApp() {
    var name = document.getElementById("name").value;
    var number = document.getElementById("number").value;

    var message = "ami add korte chai plz add koren %0AName: " + name + "%0ANumber: " + number;

    var phone = "8801628801587";

    var url = "https://wa.me/" + phone + "?text=" + message;

    window.open(url, "_blank");
}
</script>

</body>
</html>
