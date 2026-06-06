<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Will You Marry Me?</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    font-family:Arial,sans-serif;
    background:linear-gradient(to bottom,#ffe6ec,#fff);
    overflow:hidden;
}

h1{
    color:#e91e63;
    font-size:3rem;
    text-align:center;
}

.buttons{
    position:relative;
    margin-top:20px;
}

button{
    padding:15px 35px;
    font-size:22px;
    border:none;
    border-radius:12px;
    cursor:pointer;
    margin:10px;
}

#yes{
    background:#ff4081;
    color:white;
}

#no{
    background:#ff8fa3;
    color:white;
    position:absolute;
}

#message{
    margin-top:30px;
    font-size:30px;
    color:#e91e63;
    display:none;
}
</style>
</head>

<body>

<h1>Will You Marry Me? 💍❤️</h1>

<div class="buttons">
    <button id="yes">Yes</button>
    <button id="no">No</button>
</div>

<div id="message">
    ❤️ Yaaay! I can't wait to spend my life with you ❤️
</div>

<script>
const noBtn = document.getElementById("no");
const yesBtn = document.getElementById("yes");
const message = document.getElementById("message");

noBtn.addEventListener("mouseover", () => {
    const x = Math.random() * (window.innerWidth - 120);
    const y = Math.random() * (window.innerHeight - 80);

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
});

yesBtn.addEventListener("click", () => {
    document.body.innerHTML = `
    <div style="display:flex;justify-content:center;align-items:center;height:100vh;flex-direction:column;background:#fff0f5;font-family:Arial">
        <h1 style="color:#e91e63">💍 She Said YES! 💍</h1>
        <h2 style="color:#ff4081">Our forever starts now ❤️</h2>
    </div>`;
});
</script>

</body>
</html>
