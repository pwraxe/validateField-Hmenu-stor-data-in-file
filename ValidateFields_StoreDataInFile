<!DOCTYPE html>
<html>
	<head>
		<title>Register Us</title>
		<style type="text/css">
			
			fieldset{
				width: 500px;
				margin-top: 100px; 
			}

		</style>
	</head>
	<body>
		<?php
			include "welcome.php";
			
		?>

		<?php

			$FnameErr = $LnameErr = $EmailErr = $mobileErr = "";
			$FN = $LN = $email = $mobile = "";
			if($_SERVER["REQUEST_METHOD"] == "POST") 
			{
				
				if(empty($_POST["fname"]))
					$FnameErr = "First Name is require";
				else
					$FN = $_POST["fname"];

				if(empty($_POST["lname"]))
					$LnameErr = "Last name require";
				else
					$LN = $_POST["lname"];

				if(empty($_POST["email"]))
					$EmailErr = "Email require";
				else
					$email = $_POST["email"];

				if(empty($_POST["mobile"]))
					$mobileErr = "mobile number require";
				else
					$mobile = $_POST["mobile"];

			}
			echo "OK";

			$usersdata ="<br>Name : ".$FN." ".$LN." <br>Email ID : ".$email." <br>Mobile No. : ".$mobile;
			
			$file = fopen("UsersDetail.txt", "a") or die("unable to open file");
			fwrite($file, $usersdata);
			flush();
			fclose($file);

			




		?>

		
		<center>
			<fieldset>
				<form method="post" action="<?php $_SERVER['PHP_SELF']; ?>" >
					<?php

					?>
					<span class="error">* </span>First Name : <br>
					<input type="text" name="fname">
					<span class="error"> <?php echo "<br>".$FnameErr; ?></span>
					<br><br>

					<span class="error">* </span>Last Name : <br>
					<input type="text" name="lname">
					<span class="error"> <?php echo "<br>".$LnameErr; ?></span>
					<br><br>

					<span class="error">* </span>Email ID : <br>
					<input type="email" name="email">
					<span class="error"> <?php echo "<br>".$EmailErr; ?></span>
					<br><br>

					<span class="error">* </span>Mobile No : <br>
					<input type="number" name="mobile"> 
					<span class="error"> <?php echo "<br>".$mobileErr; ?></span>
					<br><br>

					<input type="submit" name="submit">
				</form>

			</fieldset>

		</center>




	</body>
</html>
