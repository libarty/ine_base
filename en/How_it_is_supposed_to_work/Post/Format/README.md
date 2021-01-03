# File format


When you submit a post, all content is converted to the appropriate format.
The default is the lightest format.
All files are wrapped in a .zip archive to reduce size and better file handling
Many files can include several different formats combined into a new format
Be very careful when choosing a format. Especially those who post comics or videos. If the format is incorrect, then the post will go to the [Trash](https://github.com/libarty/ine_base/en/What_is_it_for/Posts_page/Type) category
Parameters:
	Name-Conditional name characterizing its format
	Tags-Indicates a data type and its features can include several different data types
	Player-The program that displays the received files. Users can create their own players as add-ons to the program. If the addon is popular, it can be enabled as an addon by default. If several players work for the same format, then you can switch between them.
	Tools-Tools to edit the file
	Format-File formats that can be converted. Symbol "->" shows the format with which the player works
	Auto Filter-Automatically sets censorship. More info [here](https://github.com/libarty/ine_base/en/How_it_is_supposed_to_work/Post/Filter)
	Auto Cut text-The program to automatically cut text from a file for fast translation
	Some-Means that there are several files in the data array
	Mix-Means that the data array combines different file formats


[Text]
	Name:Article
	Tags:[Text]
	Format:.txt .pdf .doc .psd .epub .fb2 .pdf ->.epub
	Player:Book
	Tools:
		Change text,
		Change text font[Bold,Oblique,Strikethrough,Regular,Quotes,Code], 
		Change color [text,background],
		Add Paragraphs,
		Add Media file [type:image,video,audio, url:"id,https", size:"small,normal,big"]
		Change text position,
	Auto Filter:
		Word replacement
	Auto translater:
		Google transpater

[Image][Bitmap]
	Name:Bitmap Image
	Tags:[Image][Bitmap]
	Format:.png .jpg .avi .jpeg .gif .psd .sai .webp .pdf->.webp
	Player:Layer
	Tools:
		Fillter[Brightness, Blur, Color, Contrast]
		Draw[pen,brush]
		Crop
	Auto Filter:
		mosaic,
		image,
		blur,
		spot[color]
	Auto Cut text:
		pytesseract
[Image][Vector]
	Name:Vector Image
	Tags:[Image][Vector]
	Format:.svg .ai .psd .sai .webp .swf .pdf .ttf .json->.svg
	Player:Layer
	Tools:
		change point position 
		change color 
		change Gradient
		on/off line
		on/off mask
	Auto Filter:
		spot[color],
		image,

[Audio]
	Name:Sound
	Tags:[Audio]
	Format:.mp3 .mp4 .avi .flv .aac->.mp3
	Player:Video
	Tools:
		filter[tone, speed]
		Mounting
		Crop
		on/off voice
	Auto Filter:
		Muffling sound
	Auto Cut text:
		???

[ANIMATED][Bitmap]
	Name:Bitmap Animation
	Tags:[ANIMATED][Bitmap]
	Format:.mp3 .mp4 .FLV .AVI .gif .jpeg .flv .swf .webm->.webm
	Player:Video
	Tools:
		Fillter[Brightness, Blur, Color, Contrast]
		Crop
		Mounting
	Auto Filter:
		mosaic[Xsec],
		image[Xsec],
		blur[Xsec],
		spot[color][Xsec]
	Auto Cut text:
		???(lip reading)
[Animated][Vector]
	Name:Vector Animation
	Tags:[ANIMATED][Vector]
	Format:.swf .webp .json->.svg+.js?
	Player:Canvas?
	Tools:
		Mounting
		Crop
	Auto Filter:
		image[Xsec],
		spot[color][Xsec]
	
[Object]
	Name:3D object
	Tags:[Object]
	Format:.3ds .3mf .amf .assimp .awd .babylon .ctm .dae .drc .fbx .gltf .gcode .js .json .kmz .md2 .mmd .nrrd .obj .pcd .pdb .ply .prwm .sea .stl .svg .ttf .vrm .vtk .webm .wrl .x .blend .max->.gltf
	Player:3D scene
	Tools:
		Change position[model,bone]
		Change light[position,power]
		Change physics
		Change animation
		Change weight
		ADD Morph
		Change textures
		on/off layer
	Auto Filter:
		Box[color]
	
[Some]
	Format:->.zip
[Mix]
	Format:->.zip
	
[Text][Some]
	Name:Book
	Tags:[Text][Some]
[Image][Some]
	Name:Gallery
	Tags:[Image][Some]
	Player:Book,Layer
	Format:.pdf .psd .sai
[ANIMATED][Some]
	Name:Slicing
	Tags:[ANIMATED][Some]
	Player:Video
[ANIMATED][Audio][Mix][Some]
	Name:Album
	Tags:[ANIMATED][Audio][Mix][Some]
	Player:Video
[Object][Some]
	Name:3D project
	Tags:[Object][Some]
	Player:3D scene
[Image][Text][Mix]
	Name:Comic 
	Tags:[Image][Text][Mix]
	Player:Book,Layer
	Format:.pdf .psd .sai
[Image][Object][Mix]
	Name:Panorama
	Tags:[Image][Object][Mix]
	Player:3D scene
[ANIMATED][Audio][Mix]
	Name:Video
	Tags:[ANIMATED][Audio][Mix]
	Player:Video
	Tools:
		gagged(works only if the file is ANIMATED and Audio is of different length)
[ANIMATED][Audio][Text][Mix]
	Name:Video with subtitles
	Tags:[ANIMATED][Audio][Text][Mix]
	Player:Video
[ANIMATED][Text][Mix]
	Name:subtitles
	Tags:[ANIMATED][Text][Mix]
	Player:Video
	Format:->.srt
[ANIMATED][Object][Mix]
	Name:Animated panorama
	Tags:[ANIMATED][Object][Mix]
	Player:3D scene
[ANIMATED][Object][Audio][Mix]
	Name:Video panorama  
	Tags:[ANIMATED][Object][Audio][Mix]
	Player:3D scene
[ANIMATED][Object][Audio][Text][Mix]
	Name:Video panorama with subtitles
	Tags:[ANIMATED][Object][Audio][Text][Mix]
	Player:3D scene


[Other]
Name:Flash
Tags:[Game],[Animated][Vector],[Image][Vector],[Audio]
Player:Flash
Format:.swf

Name:Html theme
Tags:[Program]
Player:Html
 
Player:Edit code
Tags:[Game][Mix],[Program][Mix]
Format:.unitypackage .uproject .js .swf .js .py .cs .1h .html

Name:Version
Player:Edit code
Tags:[Game][Mix][Some],[Program][Mix][Some]
Format:.unitypackage .uproject .js .swf .js .py .cs .1h .html


