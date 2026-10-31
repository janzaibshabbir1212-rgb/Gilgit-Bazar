
<!DOCTYPE html>
<html>
<head>
<meta charset='utf-8'/>
<meta content='width=device-width, initial-scale=1' name='viewport'/>
<title>GB Bazar - Gilgit Baltistan Buy & Sell</title>
<style>
body{font-family:Arial,sans-serif;margin:0;background:#f5f5f5}
.header{background:#0d5c33;color:white;padding:18px;text-align:center}
.products{display:grid;grid-template-columns:1fr 1fr;gap:15px;padding:15px}
.card{background:white;border-radius:12px;overflow:hidden;box-shadow:0 2px 5px #0001}
.card img{width:100%;height:140px;object-fit:cover}
.card-body{padding:10px}
.price{color:#0d5c33;font-weight:bold;font-size:17px}
.btn{display:block;background:#25D366;color:white;text-align:center;padding:8px;margin-top:8px;border-radius:6px;text-decoration:none;font-weight:bold}
.sell-btn{position:fixed;bottom:20px;right:20px;background:#0d5c33;color:white;padding:15px 25px;border-radius:30px;border:none;font-weight:bold;cursor:pointer;z-index:999}
#formModal{display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:#0008;justify-content:center;align-items:center;z-index:1000}
.formBox{background:white;padding:20px;border-radius:15px;width:90%;max-width:350px}
.formBox input, .formBox select{width:95%;padding:10px;margin:8px 0;border:1px solid #ccc;border-radius:8px}
</style>
</head>
<body>

<div class='header'>
  <h1>GB BAZAR</h1>
  <p>Gilgit Baltistan Ka Apna OLX - 03553277037</p>
</div>

<div class='products'>
  <div class='card'>
    <img src='https://via.placeholder.com/300?text=Mobile+For+Sale'/>
    <div class='card-body'>
      <div class='price'>Rs 45,000</div>
      <div>Vivo Y20 - 4/64</div>
      <div>📍 Gilgit</div>
      <a class='btn' href='https://wa.me/923553277037'>WhatsApp</a>
    </div>
  </div>
</div>

<button class='sell-btn' onclick='openForm()'>+ SELL Karo</button>

<div id='formModal'>
  <div class='formBox'>
    <h3>Apna Product Becho</h3>
    <input id='pName' placeholder='Product ka naam'/>
    <input id='pPrice' placeholder='Qeemat'/>
    <select id='pLoc'><option>Gilgit</option><option>Hunza</option><option>Skardu</option><option>Ghizer</option><option>Nagar</option></select>
    <input id='pPhone' placeholder='Apna WhatsApp Number'/>
    <button class='btn' onclick='sendToAdmin()'>Admin ko Bhejo</button>
    <button onclick='closeForm()' style='background:none;border:none;width:100%;margin-top:10px'>Cancel</button>
  </div>
</div>

<script>
function openForm(){document.getElementById('formModal').style.display='flex'}
function closeForm(){document.getElementById('formModal').style.display='none'}
function sendToAdmin(){
  var name=document.getElementById('pName').value;
  var price=document.getElementById('pPrice').value;
  var loc=document.getElementById('pLoc').value;
  var phone=document.getElementById('pPhone').value;
  var adminNumber="923553277037"; 
  var msg="Salam GB Bazar! Mera product add karein:%0AProduct: "+name+"%0APrice: Rs "+price+"%0ALocation: "+loc+"%0ASeller Number: "+phone;
  window.open("https://wa.me/"+adminNumber+"?text="+msg, "_blank");
  closeForm();
}
</script>

</body>
</html>
