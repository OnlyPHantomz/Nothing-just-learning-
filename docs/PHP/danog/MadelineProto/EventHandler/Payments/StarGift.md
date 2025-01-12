---




## Properties
* `$limited`: `?bool` Show the gift is limited or not.
* `$soldOut`: `?bool` Show the gift is soldOut or not.
* `$id`: `int` Gift id.
* `$sticker`: `?danog\MadelineProto\EventHandler\Media\Sticker` Gift sticker info.
* `$stars`: `int` Amount of stars that need for buying this gift.
* `$availabilityRemains`: `?int` Amount of gift that left.
* `$availabilityTotal`: `?int` Amount of total gift.
* `$convertStars`: `int` 
* `$startSell`: `?int` Show timestamp for first buy of the gift
* `$endSell`: `?int` Show timestamp for last buy of the gift

## Method list:
* [`__construct(\danog\MadelineProto\MTProto $API, array $rawStarGift)`](#__construct)

## Methods:
### <a name="__construct"></a> `__construct(\danog\MadelineProto\MTProto $API, array $rawStarGift)`




Parameters:

* `$API`: `\danog\MadelineProto\MTProto`   
* `$rawStarGift`: `array`   


#### See also: 
* `\danog\MadelineProto\MTProto`




