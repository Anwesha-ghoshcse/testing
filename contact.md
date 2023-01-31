<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anwesha Ghosh - web developer </title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>
<body>
   <div class="container"> 
    <div class="slidebar slidebarGo">
        <nav>
          
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/Info.html">MyInfo</a></li>
                <li><a href="/mycv.pdf" download>Resume</a></li>
                <li><a href="/blog.html">Projects</a></li>
                <li><a href="/contact.html">Contact</a></li>
            </ul>
          
        </nav>
    </div>
    <div class="main">
        <div class="hamburger">
            <img class="ham" src="ham.png" alt="" width="35">
            <img class="cross" src="cross.png" alt="" width="33">
        </div>
        <div class="contactform">
            <h1>Contact Me For work</h1>

            <form onsubmit="sendEmail();">
                <div class="mb-4">
                    <label for="clientName" class="form-label">Name</label>
                    <input type="name" class= "form-control" id="clientName" aria-describedby="emailHelp">
                  </div>
                <div class="mb-4">
                  <label for="clientEmail1" class="form-label">Email address</label>
                  <input type="email" class= "form-control" id="clientEmail1" aria-describedby="emailHelp">
                </div>
                <div class="mb-4">
                  <label for="clientphone" class="form-label">Phoneno</label>
                  <input type="phone" class="form-control" id="clientphone">
                  <div id="emailHelp" class="form-text">We'll never share your email & phone with anyone else.</div>
                </div>
                <div class="mb-5">
                    Enquires<textarea id="message" name="my text"  cols="10" rows="10" placeholder="Enter Enquries"></textarea>
                  </div>
                <div class="mb-3 form-check">
                  <input type="checkbox" class="form-check-input" id="isclient">
                  <label class="form-check-label" for="isclient">I want you to work on a project with me</label>
                </div>
                <button type="submit" class="btn btn-primary">Submit</button>
              </form>
              <div class="social">
              <h3>View My Profile</h3>
              <a href="https://www.linkedin.com/in/anwesha-ghosh-07b437214" target="_blank" class="fa fa-linkedin"></a>
              <a href="https://www.facebook.com/anwesha.ghosh.3979489" target="_blank" class="fa fa-facebook"></a>
              <a href="https://t.me/Anushui" target="_blank" class="fa fa-telegram"></a>
            </div>
        </div>
    </div>
    <script src="script.js"></script>
    <script src=" https://smtpjs.com/v3/smtp.js"></script>
    <script>
      function sendEmail(){
        Email.send({
            Host : "smtp.elasticemail.com",
            Username : "anwesha05cse@gmail.com",
            Password : "502CD4A7C4964F827FBDA91A53EE47071DF3",
            To : 'anwesha05cse@gmail.com',
            From : Document.getElementById("clientEmail1").value,
            Subject : "New contact form enquiry",
            Body : "Name :" + document.getElementById("clientName").value + "<br> Email:"+ Document.getElementById("clientEmail1").value +"<br> Phone:" + Document.getElementById("clientphone").value + "<br> Message:" + Document.getElementById("message").value
        }).then(
        message => alert("message sent successfully")
        );
      }
    </script>
</body>
</html>