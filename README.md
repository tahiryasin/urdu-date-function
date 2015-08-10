## PHP function that returns date in Urdu language
	<?php
	function urdu_date(){

		$week = array(
			'Monday' => 'پیر',
			'Tuesday' => 'منگل',
			'Wednesday' => 'بدھ',
			'Thursday' => 'جمعرات',
			'Friday' => 'جمعه',
			'Saturday' => 'هفته',
			'Sunday' => 'اتوار'
		);

		$months = array(
			'January' => 'جنوری',
			'February' => 'فروری',
			'March' => 'مارچ',
			'April' => 'اپریل',
			'May' => 'مئی',
			'June' => 'جون',
			'July' => 'جولائی',
			'August' => ' اگست',
			'September' => ' ستمبر',
			'October' => 'اکتوبر',
			'November' => 'نومبر',
			'December' => 'دسمبر'
		);
		
		$date = $week[date('l')] ."&nbsp;". date('d') ."&nbsp;". $months[ date('F')] ."&nbsp;".date('Y')."ء" ;

		return $date;
	}
	
	// usage example
	header('Content-Type: text/html; charset=utf-8');
	echo  urdu_date();
	?>