# Letter Avatar

Provide a simple way to create letter avatar images, like those in your Gmail inbox.

## Install
	
	composer require "tequilarapido/letter-avatar"
	
## Usage 	
	
### Generate a letter avatar 
 
 	$letterAvatar = new LetterAvatar\LetterAvatar;
 	
 	$letterAvatar
 		->generate('A', 40)
 		->saveAsPng('/path/to/file.png');
 		
 	# You can pass a string, the first letter will be picked
 	
 	$letterAvatar
 		->generate($user->getFirstName(), 40)
 		->saveAsPng('/path/to/file.png');
 	
 	# If you don't specify a size, the max size will be used (240 by default)	 			
 		

### Custom font

The font used by default is Open Sans Regular from google font.
If you want, you can use any TTF font by setting the font file full path like so :

    $letterAvatar
        ->setFontFile('path/to/ttf_file.ttf')
        ->generate('B', 40)
        ->saveAsPng('/path/to/file.png');
 		
 		

### Save as jpeg

	$letterAvatar
		->generate('J')
		->saveAsJpeg('/path/to/file.jpg');	
	

### Save as png

	$letterAvatar
		->generate('J')
		->saveAsPng('/path/to/file.png');	
	


### Text color

	$letterAvatar
		->setTextColor([255, 0, 0])
		->generate('J')
		->saveAsJpeg('/path/to/file.jpg');	
		
### Background colors palette

	$letterAvatar
		->setBackgroundColors([255, 0, 0], [0, 255, 0], [0, 0, 255])
		->generate('J')
		->saveAsJpeg('/path/to/file.jpg');	


	