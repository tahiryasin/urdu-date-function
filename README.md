## PHP function that formats date in Urdu language
<?php

function format_date_urdu ($dateString) {

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

	$date = new DateTime($dateString);
	$new_date = $week[$date->format('l')] . "&nbsp;" . $date->format('d') . "&nbsp;" . 
    			$months[$date->format('F')] ."&nbsp;" . $date->format('Y') . "ء" ;

	return $new_date;
}

/*
Usage example
-------------
*/
header('Content-Type: text/html; charset=utf-8');
/* Date string can be passed in any format */
echo format_date_urdu('December 9th, 2012'); /* Returns: اتوار 09 دسمبر 2012ء

?>
