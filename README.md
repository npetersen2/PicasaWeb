# PicasaWeb
Interfacing with Picasa Web Albums made easy (https://picasaweb.google.com/). These classes allow easy access to the contents of _public_ users.

## Requirements
- [SimpleXML] library

## Usage
Default options
```php
array(
  "excluded_albums" => array('Profile Photos', 'Profile Data', 'Scrapbook Photos'),
  "recent" => true,
  "user_data_album_name" => "Profile Data",
  "profile_photos_album_name" => "Profile Photos"
);
```
Iterate over user's albums
```php
require_once 'PicasaWebUser.php';
require_once 'PicasaWebAlbum.php';
require_once 'PicasaWebPhoto.php';

$user = new PicasaWebUser("userId");

$user->fetchAlbums();
foreach ($user->albums as $album) {
  // code
}
```

## Future
- Add exception if can't load XML feed (All classes)
- crop and resize "Recent" cover photo (PicasaWebAlbum)

## Questions
Email me at nathan@npetersen.net

[SimpleXML]:http://php.net/manual/en/book.simplexml.php
