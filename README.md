Welcome to PHP::TVRage 
----------------------
### a PHP library for accessing tv show info from tvrage.com

### Example:
```php
<?php
     include('TVRage.php');

     $show = TV_Shows::findById('2930');
     print_r($show);
     $episode = $show->getEpisode(1,2);
     print_r($episode);
?>
```

### Gives you:
```php
TV_Show Object
(
    [showId] => 2930
    [name] => Buffy the Vampire Slayer
    [showLink] => http://tvrage.com/Buffy_The_Vampire_Slayer
    [country] => US
    [started] => 861519504
    [ended] => 1053414000
    [seasons] => 7
    [status] => Canceled/Ended
    [classification] => Scripted
    [network] => UPN
    [runtime] => 60
    [genres] => Array
        (
            [0] => Action
            [1] => Adventure
            [2] => Comedy
            [3] => Drama
            [4] => Mystery
            [5] => Sci-Fi
        )
        
    [airDay] => Tuesday
    [airTime] => 20:00
    [twelveHourAirTime] => 8:00 pm
)
TV_Episode Object
(
    [season] => 1
    [number] => 2
    [title] => The Harvest (2)
    [airDate] => 857980800
    [formattedAirDate] => Mon, March 10, 1997
    [url] => http://www.tvrage.com/Buffy_The_Vampire_Slayer/episodes/28078
)
```

### You can also search for TV shows:
```php
<?php
     $shows = TV_Shows::search("90210");
     //returns an array of TV_Show objects with 90210 in their title
?>
```
