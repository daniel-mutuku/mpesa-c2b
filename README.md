# MpesaC2B API
This is a PHP package for easily implementing Mpesa(Daraja) C2B checkout API.

## Features

- Initiate an STK push
- Check transaction status.


## Installation

Inorder to install:

```sh
composer require coding-sniper/mpesa-c2b
```

## Configuration
Fill in your credentials on the credentials.json file
```json
{
  "customer_key": "",
  "callback" : "",
  "customer_secret" : "",
  "partyb" : "",
  "shortcode" : "",
  "pass_key" : "",
  "country_code" : "", // eg 254 for Kenya. Don't prefix +
  "environment" : "live" //live or demo

}
```

## Usage

To perform an STK push:

```php
use CodingSniper\MpesaC2B\MpesaC2B;
$data = array("phone" => "","amount" => "","account_reference" => "", "trans_description" => "");
$mpesaC2B = new MpesaC2B();
$mpesaC2B->stkPush($data); 
```

To check the transaction status:
```php
use CodingSniper\MpesaC2B\MpesaC2B;
$checkID = ""; // the check_id
$mpesaC2B = new MpesaC2B();
$mpesaC2B->checkTrans($checkID); 
```

## License

MIT

**Free Software, Hell Yeah!**