# DNS-LAB
<img style=" " src="https://i.imgur.com/2bJp2DO.png"> 

<!---



 --->
<h1>A-Record Exercise</h1>

 <ul>
  <li>Connect/log into DC-1 as your domain admin account (mydomain.com\jane_admin) </li>
  <li>Connect/log into Client-1 as an admin (mydomain\jane_admin) </li>
   <img src="https://i.imgur.com/ejhAaRU.png ">
  <li>From Client-1 try to ping “mainframe” notice that it fails </li>
   <img src="https://i.imgur.com/IsH0xTo.png">
  <li>Nslookup “mainframe” notice that it fails (no DNS record) </li>
   <img src="https://i.imgur.com/jS0iXGY.png"> 
  <li>Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address </li>
   <img src="https://i.imgur.com/z8uF4O8.png" > 
  <li>Go back to Client-1 and try to ping it. Observe that it works </li>
  <img src="https://i.imgur.com/NtjTi1S.png"> 
   
 </ul>

 <h1>Local DNS Cache Exercise</h1>
 <ul>
  <li>Go back to DC-1 and change mainframe’s record address to 8.8.8.8 </li>
   <img src="https://i.imgur.com/QoleT6w.png">
  <li>Go back to Client-1 and ping “mainframe” again. Observe that it still pings the old address</li>
     <img src="https://i.imgur.com/3EPfg3q.png">

  <li>Observe the local dns cache (ipconfig /displaydns)</li>
     <img src="https://i.imgur.com/0YsRNZl.png">

  <li>Flush the DNS cache (ipconfig /flushdns)</li>
     <img src="https://i.imgur.com/Esry7Je.png">

  <li>Observe that the cache is empty (ipconfig /displaydns)</li>

  <li>Attempt to ping “mainframe” again. Observe the address of the new record is showing up</li>
     <img src="https://i.imgur.com/6TQo2av.png">

 </ul>


<h1>CNAME Record Exercise </h1>
<ul>
  <li> Go back to DC-1 and create a CNAME record that points the host “NumOneWeb” to “www.google.com”</li>
  <img src"https://i.imgur.com/t6C3HPm.png">
  <li> Go back to Client-1 and attempt to ping “NumOneWeb”, observe the results of the CNAME record</li>
    <img src"https://i.imgur.com/nhrPcgX.png">
  <li>On Client-1, nslookup “NumOneWeb”, observe the results of the CNAME record</li>
 <img src="https://i.imgur.com/UuMBte0.png"> 

 
</ul>
 
