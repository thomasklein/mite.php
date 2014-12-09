PHP class providing methods to easily communicate with the mite.api

mite (http://mite.yo.lk/en) is a sleek time tracking tool for teams and freelancers.

Example usage:
````php
<?php
	require_once("path_to_class/mite.php");

	$o_mite = mite::getInstance();
	$o_mite->init(<YOUR_API_KEY>,<YOUR_ACCOUNT_SUBDOMAIN>,'my_app_name/v1.2.3');
	try {
		$o_responseXML = $o_mite->sendRequest('get','/time_entries.xml');
	} catch (Exception $e) {
		echo "<p>".$e->getMessage()."</p>";
	}
?>
````
