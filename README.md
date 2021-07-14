# php-upc-checker
Just a simple checker of UPC Codes

## Installation (with composer)
```
composer require alanwhitney/php-upc-checker
```

## Usage
```php
// Class instantation
$barcode = '076683052001';
$upc = new \alanwhitney\php-upc-checker\Barcode();
$upc->setBarcode($barcode);

// Check for valid
if ($validator->isValid()) {
	echo 'Valid :)';
} else {
	echo 'Invalid :(';
}

// Get a check sum digit
$upc->setBarcode(substr($barcode, 0, -1));
$upc->addCheckSum();
echo $upc->getBarcode();

// Get a check sum and add a leading zero if needed
$upc->setBarcode(substr($barcode, 1, -1));
$upc->addZeroCheckSum();
echo $upc->getBarcode();
```

