This repository contains example [Vega](https://vega.github.io/vega/) visualizations which can be integrated into your InUse [synoptics](https://inuse.gitbook.io/docs/features/content/synoptic) and [dashboards](https://inuse.gitbook.io/docs/features/content/dashboard).

To configure a visualization:
1. Download the relevant JSON file. 
2. Edit the file and replace `model_name` by the name of the model from which to retrieve the properties values.
  
        // Which index to search
        index: "model_name"
 3. Set the various `field` variables to the relevant model properties. Look for `variable<x>` references.
 
       ```
       
       {
            time_buckets: {
              sum: {
              // Target 
                field: "variable1"
              }
            },
            time: {
              sum: {
                field: "variable2"
              }
            }
          } 
        }
       
  4. Add a Vega element in the target synoptic or dashboard.
  5. Copy and paste the file content into the definition text box of the element.

# Gallery

|   |   |  |
| :---: | :---: | :---: |                                     
| ![gauge1](gauge1.png) | ![fft1](fft1.png) |  | 
| [Simple gauge](./gauge1.json) | [Spectral representation](./fft1.json) |  |


# Contributing

General process to contibute a public Github repository
1. Fork this repository
2. Push your contribution to the forked repo
3. Create a pull request onto the origin repo

Useful details can be found [here](https://akrabat.com/the-beginners-guide-to-contributing-to-a-github-project/).

To add a visualization:
1. Edit your original JSON and rename the required `index` and `field` elements as described above.
2. Comment the various configuration sections. Be liberal with comments!
3. Create a visualization snipet for the gallery.
4. Edit the Gallery section of this file.
5. Commit

