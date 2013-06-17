
Grid component
--------------

Plugin page: [http://artifacts.griffon-framework.org/plugin/jgrid](http://artifacts.griffon-framework.org/plugin/jgrid)


[Grid][1] component for Swing. The site [http://www.guigarage.com][2] has some tutorials and code samples.

Usage
-----

The following nodes will become available on a View script upon installing this plugin

| *Node*  | *Type*                      |
| ------- | --------------------------- |
| jgrid   | `com.guigarage.jgrid.JGrid` |

The plugin includes sources and javadocs from the JGrid project.

### Examples

Here's the first tutorial reproduced as a Griffon application

        application(title: 'grid',
          preferredSize: [320, 240],
          pack: true,
          locationByPlatform:true,
          iconImage: imageIcon('/griffon-icon-48x48.png').image,
          iconImages: [imageIcon('/griffon-icon-48x48.png').image,
                       imageIcon('/griffon-icon-32x32.png').image,
                       imageIcon('/griffon-icon-16x16.png').image]) {
            scrollPane {
                jgrid(id: 'grid') {
                    (1..100).each { index ->
                        grid.model << index    
                    }
                }
            }
        }

[1]: http://code.google.com/p/jgrid/
[2]: http://www.guigarage.com/

