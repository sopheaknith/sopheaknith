<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.7.0/jquery.min.js"></script>
</head>
<body>
    <input type="text" name="" id="txt1">+
    <input type="text" id="txt2">=
    <input type="text" id="txt3">
    <button id="btn1">click</button>
</body>
<script>
    $(document).ready(function(){
        var txt1 =$("#txt1");
        var txt2 =$("#txt2");
        var txt3 =$("#txt3");
            $("#txt1").keyup(function(){
            txt3.val(getTotal(txt1.val(),txt2.val()));
        });
        $("#txt2").keyup(function(){
            txt3.val(getTotal(txt1.val(),txt2.val()));
        });
        function getTotal(t1,t2){
            return parseInt(t1)+parseInt(t2);
        }
    })
    </script>
</html>
