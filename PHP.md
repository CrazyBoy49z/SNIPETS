------------------
MAIL
------------------
    $message = "Сообщение с сайта - ".date('h:i:s');
		$to      = "xround2303@gmail.com";
		$from    = "info@gorky-store.ru";
		$subject = "Заказ на сайте - ".$_SERVER['HTTP_HOST'];
		$headers = "From: $from\r\nReply-to: $from\r\nContent-type: text/plain; charset=utf-8\r\n";
		$result  = mail($to, $subject, $from, $message, $headers);
