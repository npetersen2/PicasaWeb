# PicasaWeb
Interfacing with PicasasWeb made easy. These classes allow easy access to the contents of _public_ users.

## Requirements
- SimpleXML [library]

## Usage
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

[library]:http://php.net/manual/en/book.simplexml.php
