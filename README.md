# Art Book Next ([RetroPie](https://retropie.org.uk/) Version)
A simple theme for the version of EmulationStation used in [RetroPie](https://retropie.org.uk/).  
Based on the style of a coffee table book.

## Preview

![art-book-next-overview](https://user-images.githubusercontent.com/1454947/175847449-c7dec52e-e2ac-4e51-b578-6d98a9b7e68c.png)

## Configuration Options 

| AR | Gamelist - Metadata On | Gamelist - Metadata Off |
|----|----|----|
| 16:9 | ![art-book-next-16-9-metadata-on](https://user-images.githubusercontent.com/1454947/175848140-4b202408-52ba-42d8-a8c8-8cfa95d9b8fb.png) | ![art-book-next-16-9-metadata-off](https://user-images.githubusercontent.com/1454947/175848185-3a630599-e954-4dc7-8e7a-a385c97436fd.png) |
| 16:10 | ![art-book-next-16-10-metadata-on](https://user-images.githubusercontent.com/1454947/175848326-e77272eb-4370-43a9-ae12-7d7a5a79728c.png) | ![art-book-next-16-10-metadata-off](https://user-images.githubusercontent.com/1454947/175848355-5696ed70-52a3-4bc9-9c81-0fe7e1a1a5d7.png) |
| 4:3 | ![art-book-next-4-3-metadata-on](https://user-images.githubusercontent.com/1454947/175848384-cc4529e1-bded-417b-a823-8894fece0c38.png) | ![art-book-next-4-3-metadata-off](https://user-images.githubusercontent.com/1454947/175848424-a49ed090-f49f-456b-bb42-8e88229d0309.png) |

The above options can be set by editing the theme.xml. 
Open theme.xml and look for this section:
```
<variables>
  <!-- 
  Apsect Ratio Options:
  16:10 = 16-10
  16:9 = 16-9
  4:3 = 4-3
  --><aspectRatio>16-9</aspectRatio>
  <!-- 
  Gamelist Style Options:
  metadata-off
  metadata-on
  --><gameListStyle>metadata-on</gameListStyle>
  <logoFont>./_inc/fonts/ChangaOne-Italic.ttf</logoFont>
  <bodyFont>./_inc/fonts/Oxygen-Bold.ttf</bodyFont>
  <spacerImage>./_inc/images/utility/space.png</spacerImage>
</variables>
```
- To set aspect ratio change `<aspectRatio>16-9</aspectRatio>` to 16-9, 16-10 or 4-3 (please make sure to match the aspect ratio to your screen)
- To set change the gamelist style change `<gameListStyle>metadata-on</gameListStyle>` to metadata-on or metadata-off

## Details

- Supports 16:9, 16:10 and 4:3 aspect ratios (please set the AR that matches your display using the instructions above) 
- 2 gamelist view styles available (1) "Metadata On" and (2) "Metadata Off" (see screenshots above)
- Includes logos and artwork for all available systems in RetroPie
