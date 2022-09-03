<!-- Hi I am Rosa (Cambodian) -->
<!-- Calculator using PHP -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
</head>
<body>
    <form action="" method="post">
        <h1 style="text-align:center;">Welcome To online calculator</h1>
        <ol style="list-style:none">
            <li style="padding:10px 0px;">
                <strong>Number 1 : </strong>
                <input type="number" name="nb1">
            </li>
            <li>
                <strong>Number 2 : </strong>
                <input type="number" name="nb2">
            </li>
            <li style="background-color:skyblue; width:29%">
                <p style="color:white">Option</p>
                <ol type="1">
                    <!-- <li>Plus (+)</li>
                    <li>Minus (-)</li>
                    <li>Multiply (*)</li>
                    <li>Devide (/)</li> -->
                    <li style="list-style:none">
                        <select name="option" id="">
                            <option value="0" hidden="0">------ choose ------</option>
                            <option value="Plus" >( + ) Plus</option>
                            <option value="Minus">( - ) Minus</option>
                            <option value="Multiply">( * ) Multiply</option>
                            <option value="Devide">( / ) Devide </option>
                            <option value="Exponentiation">( ^ ) Exponentiation</option>
                        </select>
                    </li>
                </ol>
            </li>
            <li style="padding:10px 0px 0 100px; ">
                <input type="submit" name="btnanswer" 
                    style="background-color:red;color:white;border:3px solid gray;
                        cursor:pointer;border-radius:5px;width:90px;height:40px;">
            </li>
        </ol>
    </form>
    <div style="background-color:gray;color:yellow;font-size:1.3em;
            width:90%;height:auto;padding:0 50px;" >
        <?php
            if(isset($_POST['btnanswer']))
            {
                $number1 = $_POST['nb1'];
                $number2 = $_POST['nb2'];
                $option = $_POST['option'];
                switch($option)
                {
                    case "Plus":
                        $result = $number1 + $number2;
                        break;
                    case "Minus":
                        $result = $number1 - $number2;
                        break;
                    case "Multiply":
                        $result = $number1 * $number2;
                        break;
                    case "Devide":
                        $result = $number1 / $number2;
                        break;
                    case "Exponentiation":
                        $result = $number1 ** $number2;
                        break;
                }
                echo "Number 1 : $number1";
                echo "<br>Number 2 : $number2";
                echo "<br>Option : $option";
                echo "<style>background-color:red;</style>"."<br><br>Result : $result";

            }




        ?>
    </div>
    
</body>
</html>
