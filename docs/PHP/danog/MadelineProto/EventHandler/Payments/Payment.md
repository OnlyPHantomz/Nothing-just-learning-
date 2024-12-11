---
title: "danog\\MadelineProto\\EventHandler\\Payments\\Payment: This object contains information about an incoming pre-checkout query."
description: ""
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\EventHandler\Payments\Payment`
[Back to index](../../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

This object contains information about an incoming pre-checkout query.  



## Properties
* `$queryId`: `int` Unique query identifier
* `$userId`: `int` User who sent the query
* `$payload`: `string` Bot specified invoice payload
* `$info`: `?danog\MadelineProto\EventHandler\Payments\PaymentRequestedInfo` Order info provided by the user
* `$shippingOptionId`: `?string` Identifier of the shipping option chosen by the user
* `$currency`: `string` Three-letter ISO 4217 currency code
* `$totalAmount`: `int` 

## Method list:
* [`accept(): true`](#accept)
* [`reject(string $errorMessage): false`](#reject)

## Methods:
### <a name="accept"></a> `accept(): true`

Accept pending payment.
note that you must call this function or reject function up to 10 seconds after user accept payment!!.  



### <a name="reject"></a> `reject(string $errorMessage): false`

Reject pending payment.
note that you must call this function or accept function up to 10 seconds after user accept payment!!.  


Parameters:

* `$errorMessage`: `string` if the success isn’t set. Error message in human-readable form that explains the reason for failure to proceed with the checkout  



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)