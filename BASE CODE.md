### &#x20;                                       **BASE CODE**







**HTML:**



&#x20;    **<!DOCTYPE html>**

**<html>**

**<head>**

&#x20;   **<title>Hospital Bed Availability Board</title>**

&#x20;   **<link rel="stylesheet" href="style.css">**

**</head>**

**<body>**



**<h1>Hospital Bed Availability Board</h1>**



**<!-- Filters -->**

**<div class="box">**

&#x20;   **<h2>Filter</h2>**



&#x20;   **<select>**

&#x20;       **<option>All Wards</option>**

&#x20;       **<option>General Ward</option>**

&#x20;       **<option>ICU</option>**

&#x20;   **</select>**

**</div>**



**<!-- Bed Status -->**

**<div class="box">**

&#x20;   **<h2>Bed Status</h2>**



&#x20;   **<table>**

&#x20;       **<tr>**

&#x20;           **<th>Ward</th>**

&#x20;           **<th>Total</th>**

&#x20;           **<th>Available</th>**

&#x20;       **</tr>**



&#x20;       **<tr>**

&#x20;           **<td>General</td>**

&#x20;           **<td>100</td>**

&#x20;           **<td id="general">55</td>**

&#x20;       **</tr>**



&#x20;       **<tr>**

&#x20;           **<td>ICU</td>**

&#x20;           **<td>20</td>**

&#x20;           **<td id="icu">8</td>**

&#x20;       **</tr>**

&#x20;   **</table>**

**</div>**



**<!-- CRUD -->**

**<div class="box">**

&#x20;   **<h2>Bed Status CRUD</h2>**



&#x20;   **<button>Add</button>**

&#x20;   **<button>Update</button>**

&#x20;   **<button>Delete</button>**

**</div>**



**<!-- Public Map -->**

**<div class="box">**

&#x20;   **<h2>Public Map</h2>**



&#x20;   **<p>Hospital Location Map</p>**



&#x20;   **<iframe**

&#x20;       **src="https://maps.google.com/maps?q=Chennai\&t=\&z=13\&ie=UTF8\&iwloc=\&output=embed"**

&#x20;       **width="100%"**

&#x20;       **height="250">**

&#x20;   **</iframe>**



**</div>**



**<!-- API -->**

**<div class="box">**

&#x20;   **<h2>Update API</h2>**



&#x20;   **<button onclick="updateData()">Refresh Data</button>**

**</div>**



**<!-- Audit -->**

**<div class="box">**

&#x20;   **<h2>Audit Log</h2>**



&#x20;   **<ul id="audit">**

&#x20;       **<li>System Started</li>**

&#x20;   **</ul>**

**</div>**



**<!-- Role -->**

**<div class="box">**

&#x20;   **<h2>Role Based Access</h2>**



&#x20;   **<button>Admin</button>**

&#x20;   **<button>Public</button>**

**</div>**



**<script src="script.js"></script>**



**</body>**

**</html>**







**CSS:**

&#x20;   **body{**

&#x20;   **font-family:Arial;**

&#x20;   **background:#f2f2f2;**

&#x20;   **margin:20px;**

**}**



**h1{**

&#x20;   **text-align:center;**

**}**



**.box{**

&#x20;   **background:white;**

&#x20;   **padding:15px;**

&#x20;   **margin:20px auto;**

&#x20;   **width:80%;**

&#x20;   **border-radius:8px;**

&#x20;   **border:1px solid #ccc;**

**}**



**table{**

&#x20;   **width:100%;**

&#x20;   **border-collapse:collapse;**

**}**



**table,th,td{**

&#x20;   **border:1px solid gray;**

**}**



**th,td{**

&#x20;   **padding:10px;**

&#x20;   **text-align:center;**

**}**



**button{**

&#x20;   **padding:10px 20px;**

&#x20;   **margin:5px;**

&#x20;   **cursor:pointer;**

**}**



**select{**

&#x20;   **padding:8px;**

**}**







**JAVA SCRIPT:**

&#x20;           **function updateData(){**



&#x20;   **let general=Math.floor(Math.random()\*100);**



&#x20;   **let icu=Math.floor(Math.random()\*20);**



&#x20;   **document.getElementById("general").innerHTML=general;**



&#x20;   **document.getElementById("icu").innerHTML=icu;**



&#x20;   **let log=document.getElementById("audit");**



&#x20;   **let item=document.createElement("li");**



&#x20;   **item.innerHTML="Bed status updated.";**



&#x20;   **log.appendChild(item);**



**}**

