<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>WhatsApp Submit Form</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            font-family: Arial, sans-serif;

            /* Advanced Background */
            background:
                radial-gradient(circle at top left, #6a11cb 0%, transparent 35%),
                radial-gradient(circle at bottom right, #2575fc 0%, transparent 40%),
                linear-gradient(135deg, #0f172a, #1e293b, #111827);

            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        /* Main DIV Container */
        .main-container {
            width: 100%;
            max-width: 420px;

            background: rgba(255, 255, 255, 0.10);
            backdrop-filter: blur(18px);

            border: 1px solid rgba(255, 255, 255, 0.2);

            border-radius: 25px;
            padding: 35px 25px;

            box-shadow:
                0 20px 50px rgba(0, 0, 0, 0.5),
                inset 0 1px 1px rgba(255, 255, 255, 0.2);

            color: white;
        }

        /* Avatar DIV */
        .avatar-box {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }

        .avatar-box img {
            width: 100px;
            height: 100px;

            border-radius: 50%;
            object-fit: cover;

            border: 4px solid #ffffff;

            box-shadow:
                0 0 20px #00f2fe,
                0 0 40px rgba(0, 242, 254, 0.5);
        }

        /* Title */
        .title {
            text-align: center;
            font-size: 26px;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .subtitle {
            text-align: center;
            color: #cbd5e1;
            font-size: 14px;
            margin-bottom: 25px;
        }

        /* Form DIV */
        .form-group {
            margin-bottom: 18px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-size: 14px;
            font-weight: bold;
        }

        input,
        textarea {
            width: 100%;

            background: rgba(255, 255, 255, 0.12);
            color: white;

            border: 1px solid rgba(255, 255, 255, 0.25);

            border-radius: 12px;

            padding: 14px;

            outline: none;

            font-size: 15px;

            transition: 0.3s;
        }

        input::placeholder,
        textarea::placeholder {
            color: #cbd5e1;
        }

        input:focus,
        textarea:focus {
            border-color: #00f2fe;

            box-shadow:
                0 0 10px rgba(0, 242, 254, 0.5);
        }

        textarea {
            height: 120px;
            resize: none;
        }

        /* Unique Submit Button */
        .whatsapp-submit-btn {
            width: 100%;

            padding: 15px;

            border: none;
            border-radius: 14px;

            background: linear-gradient(
                135deg,
                #25D366,
                #128C7E
            );

            color: white;

            font-size: 17px;
            font-weight: bold;

            cursor: pointer;

            position: relative;
            overflow: hidden;

            transition: 0.3s;

            box-shadow:
                0 10px 25px rgba(37, 211, 102, 0.35);
        }

        /* Button Shine Effect */
        .whatsapp-submit-btn::before {
            content: "";

            position: absolute;

            top: 0;
            left: -100%;

            width: 100%;
            height: 100%;

            background: linear-gradient(
                90deg,
                transparent,
                rgba(255,255,255,0.4),
                transparent
            );

            transition: 0.5s;
        }

        .whatsapp-submit-btn:hover::before {
            left: 100%;
        }

        .whatsapp-submit-btn:hover {
            transform: translateY(-3px);

            box-shadow:
                0 15px 35px rgba(37, 211, 102, 0.55);
        }

        .whatsapp-submit-btn:active {
            transform: scale(0.97);
        }

        .footer-text {
            text-align: center;
            margin-top: 18px;

            font-size: 12px;
            color: #94a3b8;
        }
    </style>
</head>

<body>

    <!-- Main DIV -->
    <div class="main-container">

        <!-- Avatar DIV -->
        <div class="avatar-box">

            <!-- এখানে আপনার Avatar Image SRC Link দিন -->
            <a href="https://ibb.co.com/WNpgzjMy"><img src="https://i.ibb.co.com/DPg5MTvC/i-Phone-Vivid-Mazhar-Pictures-LMC-20260322-173520-i-Phone-Vivid-Mazhar-Pictures-LMC-PORTRAIT.jpg" alt="i-Phone-Vivid-Mazhar-Pictures-LMC-20260322-173520-i-Phone-Vivid-Mazhar-Pictures-LMC-PORTRAIT" border="0"></a>

        </div>

        <h1 class="title">Contact Us</h1>

        <p class="subtitle">
            Send your message directly to WhatsApp
        </p>


        <!-- Form DIV -->
        <div class="form-group">

            <label>Your Name</label>

            <input
                type="text"
                id="name"
                placeholder="Enter your name"
            >

        </div>


        <div class="form-group">

            <label>Your Message</label>

            <textarea
                id="message"
                placeholder="Write your message..."
            ></textarea>

        </div>


        <!-- Unique Submit Button -->
        <button
            class="whatsapp-submit-btn"
            onclick="sendToWhatsApp()"
        >
            🚀 SUBMIT TO WHATSAPP
        </button>


        <div class="footer-text">
            Secure • Fast • Direct WhatsApp Message
        </div>

    </div>


    <!-- JavaScript -->
    <script>

        function sendToWhatsApp() {

            let name =
                document.getElementById("name").value.trim();

            let message =
                document.getElementById("message").value.trim();


            /* Validation */

            if (name === "") {
                alert("Please enter your name!");
                return;
            }

            if (message === "") {
                alert("Please enter your message!");
                return;
            }


            /* WhatsApp Number */

            let phoneNumber = "8801628801587";


            /* Create Message */

            let whatsappMessage =
                "👤 *New Form Submission*%0A%0A" +
                "📝 *Name:* " + name + "%0A%0A" +
                "💬 *Message:* " + message;


            /* WhatsApp URL */

            let whatsappURL =
                "https://wa.me/" +
                phoneNumber +
                "?text=" +
                encodeURIComponent(
                    "👤 New Form Submission\n\n" +
                    "📝 Name: " + name +
                    "\n\n💬 Message: " + message
                );


            /* Open WhatsApp */

            window.open(
                whatsappURL,
                "_blank"
            );

        }

    </script>

</body>
</html>
