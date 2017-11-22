------------------
MAIL
------------------
	function send_mail(){
		$message = "Сообщение с сайта - ".date('h:i:s');
		$to      = "xround2303@gmail.com";
		$from    = "info@gorky-store.ru";
		$subject = "Заказ на сайте - ".$_SERVER['HTTP_HOST'];
		$headers = "From: $from\r\nReply-to: $from\r\nContent-type: text/plain; charset=utf-8\r\n";
		$result  = mail($to, $subject, $from, $message, $headers);

		if($result){
			echo 'Письмо отправленно';
		}else{
			echo 'Ошибка при отправке письма';
		}
	}

------------------
ОТОБРАЖЕНИЕ ОШИБОК
------------------
	ini_set('error_reporting', E_ALL);
	ini_set('display_errors', 1);
	ini_set('display_startup_errors', 1);
    	
