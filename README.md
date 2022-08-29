# Art Book Next (RetroPie Version)
A simple theme for the version of EmulationStation used in [RetroPie](https://retropie.org.uk/).  
Based on the style of a coffee table book.

Discussion occuring here: https://retropie.org.uk/forum/topic/33010/theme-art-book-next

## **Preview**

| System View | Gamelist View |
|----|----|
| ![Screen Shot 2022-07-21 at 12 51 34](https://user-images.githubusercontent.com/1454947/180350112-d2d1f712-3fd2-4177-8007-4e60b37118a6.png) | ![Screen Shot 2022-07-21 at 12 47 54](https://user-images.githubusercontent.com/1454947/180350136-649904ec-9563-48e7-9976-3219326e2156.png) |

## **Configuration Options**

- The theme has a simple set of options that can be changed directly in the root theme.xml 
   - Options:
   - `<aspectRatio></aspectRatio>`- sets the aspect ratio the theme will render at. If needed, this should be changed to match the aspect ratio of your screen.
   - `<gameListStyle></gameListStyle>`- sets the layout used for the gamelist view when media & metadata are scraped for your games
   - `<colorScheme></colorScheme>`- sets the color scheme that is used for the overall theme on all views
- 16:9, 16:10 and 4:3 aspect ratios are currently supported
- there are 2 gamelist layouts to choose from (metadata-on & metadata-off)
- and 4 pre-built color schemes are currently available with the option of creating your own customized color scheme through a simple XML file (details below)

### Preview of the Aspect Ratio & Layout Variants

| Aspect Ratio | Gamelist - Metadata On | Gamelist - Metadata Off |
|----|----|----|
| 16:9 | ![art-book-next-16-9-metadata-on](https://user-images.githubusercontent.com/1454947/175848140-4b202408-52ba-42d8-a8c8-8cfa95d9b8fb.png) | ![art-book-next-16-9-metadata-off](https://user-images.githubusercontent.com/1454947/175848185-3a630599-e954-4dc7-8e7a-a385c97436fd.png) |
| 16:10 | ![art-book-next-16-10-metadata-on](https://user-images.githubusercontent.com/1454947/175848326-e77272eb-4370-43a9-ae12-7d7a5a79728c.png) | ![art-book-next-16-10-metadata-off](https://user-images.githubusercontent.com/1454947/175848355-5696ed70-52a3-4bc9-9c81-0fe7e1a1a5d7.png) |
| 4:3 | ![art-book-next-4-3-metadata-on](https://user-images.githubusercontent.com/1454947/175848384-cc4529e1-bded-417b-a823-8894fece0c38.png) | ![art-book-next-4-3-metadata-off](https://user-images.githubusercontent.com/1454947/175848424-a49ed090-f49f-456b-bb42-8e88229d0309.png) |

### Preview of the pre-built Color Schemes

| Color | Preview |
|----|----|
| Art Book Next  | ![art-book-next-16-9-metadata-on](https://user-images.githubusercontent.com/1454947/175848140-4b202408-52ba-42d8-a8c8-8cfa95d9b8fb.png) |
| Art Book (based on my original theme from [2017](https://retropie.org.uk/forum/topic/11728/theme-art-book)) | ![Screen Shot 2022-07-21 at 12 11 33](https://user-images.githubusercontent.com/1454947/180265407-3ad891fd-2180-4054-8322-891bfdb20ca1.png) |
| Steam OS (being used as the default for [RetroDeck](https://github.com/XargonWan/RetroDECK/)) | ![Screen Shot 2022-07-21 at 12 13 12](https://user-images.githubusercontent.com/1454947/180265431-719688ab-6b6b-4c68-821d-77b7a6da7c1e.png) | 
| SNES (simply made for fun as the SNES was my first console) | ![Screen Shot 2022-07-21 at 12 12 26](https://user-images.githubusercontent.com/1454947/180265452-4a687612-d138-4e15-89bf-dc082f45f155.png) |

## User Customizations
When using the theme on RetroPie you can make the following changes in the root theme.xml to tailor the look to your setup

### Aspect Ratio... 
Change the value in `<aspectRatio>` to match your screen aspect ratio (default is 16-9)
```
<!-- 
Apsect Ratio Options:
16:10 = 16-10
16:9 = 16-9
 4:3 = 4-3
-->
<aspectRatio>16-9</aspectRatio>
```

### Gamelist Style... 
Change the value in `< gameListStyle >` to match your preferred gamelist layout (default is metadata-on)
```
<!-- 
Gamelist Style Options:
metadata-off
metadata-on
-->
<gameListStyle>metadata-on</gameListStyle>
```

### Color Scheme...
Change the value in `< colorScheme >` to match your preferred color scheme (default is art-book-next)
```
<!-- 
Color Scheme Options:
art-book-next
art-book
snes
steam-deck
custom
-->
<colorScheme>art-book-next</colorScheme>
```
If you change the color scheme option to `custom` then you can change values in the `color-scheme-custom.xml` file to match the colors you prefer.  I am happy to add additional colors to the pre-built list too; so if you create one that you are comfortable with sharing please post it here: https://retropie.org.uk/forum/topic/33010/theme-art-book-next

### Example:
As a quick example if you have a screen with a 16:10 aspect ratio, do not want to see metadata and like the snes colors then this is what you would change in the theme.xml

```
<!-- 
Apsect Ratio Options:
16:10 = 16-10
16:9 = 16-9
4:3 = 4-3
-->
<aspectRatio>4-3</aspectRatio>
<!-- 
Gamelist Style Options:
metadata-off
metadata-on
-->
<gameListStyle>metadata-off</gameListStyle>
<!-- 
Color Scheme Options:
art-book-next
art-book
snes
steam-deck
custom
-->
<colorScheme>snes</colorScheme>
```

## **To-Do**
(a quick list of items I am looking to add)
* Add 3:2 & 5:3 Aspect Ratios
* Create and add any missing background art
* Add the ability to provide custom background art

## **Additional Notes**

### Scraping:
* To create the layout in the metadata-on variation i rely on the md_thumbnail, md_video and md_marquee tags.  So to get the same look these are my recommended scrape settings:
   * `md_image` = screenshot
   * `md_marquee` = wheel (the transparent wheel art)
   * `md_thumbnail` = 2D boxart
   * `md_video` = video (though this is optional as the theme also works with just md_image)

### Versions for other ES forks:
* If you use ES-DE... then this version of the theme will work out of the box with that distribution.  When used with ES-DE the theme comes with additional support for navigation sound sets.  I'm also working on a version to support the 2.0 theme engine that the ES-DE team is working on and will post that here when available.
* If you use Batocera... then check out the version [here](https://github.com/anthonycaccese/es-theme-art-book-next/archive/2.0.zip).  The Batocera version has all the same base features but simply makes them available to change through Batocera's menu UI (i.e. you don't need to touch the XML as discussed above).  It also adds some additional features such as the theming of the menu and the ability to toggle on/off the display of different media elements directly through the menu ui as well.

## **Acknowledgments**
* Most system logos were sourced and modified from the excellent work done by Dan Patrick [here](https://archive.org/details/console-logos-professionally-redrawn-plus-official-versions).  I modified each to be compatible with EmulationStation's current SVG support.
* ChangaOne font is by [Eduardo Tunni](https://www.fontsquirrel.com/fonts/changa)
* Oxygen font is by [Vernon Adams](https://www.fontsquirrel.com/fonts/oxygen)

## **License**
Creative Commons CC-BY-NC-SA - https://creativecommons.org/licenses/by-nc-sa/2.0/
You are free to share and adapt this theme as long as you provide attribution back to me (and the above credits) as well share any updates you make under the same licence terms.

## **Download**
For Retropie and ES-DE v1.x - https://github.com/anthonycaccese/art-book-next-retropie/archive/master.zip

Thank you for taking a look at this 😄
