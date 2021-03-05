
<!DOCTYPE html>
<html lang="en" dir="ltr">
   <head>
     <meta charset="utf-8">

     <title>PIGGYBANK</title>
     <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
     <style>
         button {border: 5px solid pink;
                 border-radius:20px}
         p.short{width:70px;
                 height:20px;
                 border: 5px solid pink;
                 margin:20px;
                 border-radius:20px;
                 text-align: center;}
     </style>

  </head>
 <body background ="https://media.coindesk.com/uploads/2017/08/piggy-bank-e1504182200356.jpg">

       <h1><font color = "pink">Stashing away for your little pigglets</font></h1>
       <h3><font color = "pink">Earn 10% APY on your savings</font></h3>

   <div style="right:20px;padding:30px"></div>

          <input id = "deposit" placeholder = "Add amount" type = "number" >
          <button style = "background-color: pink" id = "btn"
          >Add to your Piggy Bank</button>
          <p class = "short" id = "PIGGYBANK"></p>

   <div style="right:20px;padding:50px"></div>

          <button style = "background-color: pink" id = "addUP">Show my savings after 1 year</button>
          <p class = "short" id = "SITotal"></p>


     <script>
     var depoArray = [];

     $("#btn").click(function(){
      var userDeposit = $("#deposit").val();
     depoArray.push(parseInt(userDeposit));
      console.log(depoArray);
      var sum = depoArray.reduce(depoArr);
     function depoArr(total, value, index, array) {
     return total + value;
     }
       document.getElementById("PIGGYBANK").innerHTML = sum;
     });


     function depoArr(total, value, index, array) {
      return total + value;
     }


     $("#addUP").click(function SI(){
     var P =   depoArray.reduce(depoArr)//$("#deposit").val();
     var R = 10;
     var T = 1;
     var SI = P*R*T/100;
     var To = parseInt(P) + SI;
     //alert(To);
         document.getElementById("SITotal").innerHTML = To;

     });
   </script>


 </body>
</html>
