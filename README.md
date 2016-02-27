<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <style>td{height: 20px;width: 20px;border: 1px solid black; } </style>
    </head>
    <body>
<div id="table"></div>
       <div id="azaza" style="height:20px; width:20px;"></div>
        <script>
            
            //рандом
            var letter = new Array();
            letter[0] = "ф";
            letter[1] = "б";
            letter[2] = "в";
            letter[3] = "г";
            letter[4] = "д";
            letter[5] = "е";
            letter[6] = "ё";
            letter[7] = "ж";
            letter[8] = "з";
            letter[9] = "и";
            letter[10] = "й";
        var randomLetter = (letter[Math.round(Math.random()*10)]);
            
            
            
            //таблица
            var t = document.createElement("table");
            var tbody = document.createElement("tbody");
            
            for(var i = 0;i<10;i++) {

                var tr = document.createElement('tr');
                
                for (var j = 0;j<10;j++){
                    var td = document.createElement('td');
                    td.innerHTML = randomLetter;
                    tr.appendChild(td);
                }
                   tbody.appendChild(tr);
            }
            
            t.appendChild(tbody);
            document.getElementById('table').appendChild(t);
           
            
            
            
            //смена фона
            function rndColor() {
            var r = Math.floor(Math.random()*256);
            var g = Math.floor(Math.random()*256);
            var b = Math.floor(Math.random()*256);
            var rgb = 'rgb(' + r + ',' + g + ',' + b + ')';
             
            var elements = t.getElementsByTagName('td');

            for (var i = 0; i < elements.length; i++) {
            var td = elements[i];
            alert( td.value + ': ' + td.checked );
            td.style.backgroundColor = rgb;
            }    }
            window.onload = rndColor;
        </script>
    </body>
</html>
