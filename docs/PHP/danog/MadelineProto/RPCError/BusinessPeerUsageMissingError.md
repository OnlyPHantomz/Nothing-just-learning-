---
title: "danog\\MadelineProto\\RPCError\\BusinessPeerUsageMissingError: You cannot send a message to a user through a [business connection](https://core.telegram.org/api/business#connected-bots) if the user hasn't recently contacted us."
description: "\nNote: this exception is part of the raw API, and thus is not covered by the backwards-compatibility promise.\n\nAlways check the changelog when upgrading, and use tools like Psalm to easily upgrade your code.\n"
image: "https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png"
parent: "MadelineProto API"

---
# `danog\MadelineProto\RPCError\BusinessPeerUsageMissingError`
[Back to index](../../../index.html)

> Author: Daniil Gentili <daniil@daniil.it>  
  

You cannot send a message to a user through a [business connection](https://core.telegram.org/api/business#connected-bots) if the user hasn't recently contacted us.  


Note: this exception is part of the raw API, and thus is not covered by the backwards-compatibility promise.

Always check the changelog when upgrading, and use tools like Psalm to easily upgrade your code.


## Properties
* `$rpc`: `string` RPC error.
* `$description`: `string` Human-readable description of RPC error.
* `$tlTrace`: `string` TL trace.

## Method list:
* [`getLocalization(): string`](#getLocalization)
* [`getMessage(): string`](#getMessage)
* [`getCode()`](#getCode)
* [`getFile(): string`](#getFile)
* [`getLine(): int`](#getLine)
* [`getTrace(): array`](#getTrace)
* [`getPrevious(): ?Throwable`](#getPrevious)
* [`getTraceAsString(): string`](#getTraceAsString)
* [`getTLTrace(): string`](#getTLTrace)

## Methods:
### <a name="getLocalization"></a> `getLocalization(): string`

Get localized error name.



### <a name="getMessage"></a> `getMessage(): string`





### <a name="getCode"></a> `getCode()`





### <a name="getFile"></a> `getFile(): string`





### <a name="getLine"></a> `getLine(): int`





### <a name="getTrace"></a> `getTrace(): array`





### <a name="getPrevious"></a> `getPrevious(): ?Throwable`




#### See also: 
* `Throwable`




### <a name="getTraceAsString"></a> `getTraceAsString(): string`





### <a name="getTLTrace"></a> `getTLTrace(): string`

Get TL trace.



---
Generated by [danog/phpdoc](https://phpdoc.daniil.it)