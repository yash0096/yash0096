<Html><head>
  </head>
 <body BgColor="black"><center>
   
     <input type="button"value="Toss"style="width:300px;height:120px;background-color:silver;color: white;font-size:60px;"onclick="ht()">
<script type="text/javascript">
   function ht()
   {   
        var delX=Math.random(Math.random(0.5));
    var delY=Math.random(Math.random(0.5));
    var count=0;
    var count2=0;
    var trail=prompt('enter no.of trails');
    var ontime=prompt ("ENTER-> d for details, y to see every toss, n for final result");
   var prdtoss=prompt("predict-> head or tail.?(h/t)");
    for(toss=1;toss<=trail;toss++)
    { 
    delZ=Math.random(delX+delY)*100;
    if(delZ>50)
    {
    count++;
    var h=1,t=0;
    }
    else
    {
    count2++;
    var t=1,h=0;
    }
    var ontime;
      switch(ontime)
      {
        case "d" :
                   if(count!=count2)
                   {
         document.write('<table>');
        document.write('<tr><td bgcolor="#ccffda">'+'Trail('+toss+'): Head['+count+"("+h+")"+'] , Tail['+count2+"("+t+")"+']');
        document.write('</table>');
                   }
                   else
                  {
                     document.write('<table>');
        document.write('<tr><td bgcolor="#fdffcc">'+'Trail('+toss+'): Head['+count+"("+h+")"+'] , Tail['+count2+"("+t+")"+']');
        document.write('</table>');
                  }
        break;
        case "y" :
alert('trail_'+toss+'_RESULT-Head:_'+count+'Tail:_'+count2+"TossesCompleted:"+(toss)+"_Outof:"+ trail+"_Remaining Tosses:"+(trail-toss));
        break;
        case "n" :
          if(count+count2==trail)
          {
   alert(count+' Heads and '+count2+'Tails in '+trail+'_trails'+(count/trail)*100+'% chance to get Heads and '+(1-(count/trail))*100+'% chance to get Tails');
          document.write('<table>');
        document.write('<tr><td bgcolor="#fdffcc">'+'Trail('+toss+'): Head['+count+"("+h+")"+'] , Tail['+count2+"("+t+")"+']');
        document.write('</table>');
          }
          else
          {
          count=count;
          count2=count2;
          }
       break;
       default:
               trail=0;
              document.write('<table>')
       document.write('<tr><td bgcolor="red">'+"invalid input: "+ontime);
       document.write('</table>')
       
   }
   }
   if((trail<0)||(trail==0))
   {
     if(trail==0)
     {
       alert ("coin not tossed");
     }
     else
     if(trail<0)
     {
      alert("Enter positive values");
     }
   }
   else
   if(trail>0)
  {
   trail=trail;
   document.write('<table>');
  document.write('<tr><b><td bgcolor="lightgreen">'+"Task Complete..!! :-)"+k);
   document.write('</table>');
  }
  else
 {   
  alert ("invalid input");
  document.write('<table>');
  document.write('<tr><td bgcolor="red">'+" invalid inputs_-->"+trail+",_-->"+ontime);
  document.write('</table>');
 }
   }
</script>
 </body>
         </html>
