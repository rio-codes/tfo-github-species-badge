# tfo-github-species-badge
A shields.io Github profile badge that counts members of a given species in your collection on [tfo.creaturetracker.net](https://tfo.creaturetracker.net), a breeding tracker for [The Final Outpost](https://finaloutpost.net)


## The Badge

![Ebena count](https://img.shields.io/endpoint?style=for-the-badge&logo=gunicorn&label=Ebena%20count&url=https%3A%2F%2Ftfo.creaturetracker.net%2Fapi%2Fpublic%2Fusers%2Flyricism%2Fcreature-count%3Fspecies%3DEbena%2520Kuranto&logoColor=D0BCFF)

Yup. That many horses. Look at this weird one:<br />
![https://finaloutpost.net/view/WoZK6/](https://finaloutpost.net/rimg/WoZK6.png)

## Needed Info

There are 5 essential parameters you need to construct the [shields.io](https://shields.io) URL for this badge:

- `style`
  Shields.io has the following styles:
  
    - `flat`: ![Example badge](https://img.shields.io/badge/example-badge-magenta?style=flat) (This is the default, if you leave out the `style` parameter you will get this one.
      
    - `flat-square`: ![Example badge](https://img.shields.io/badge/example-badge-magenta?style=flat-square)
      
    - `plastic`: ![Example badge](https://img.shields.io/badge/example-badge-magenta?style=plastic)
      
    - `for-the-badge`: ![Example badge](https://img.shields.io/badge/example-badge-magenta?style=for-the-badge) (This is the the one I use)
      
    - `social`: ![Example badge](https://img.shields.io/badge/example-badge-magenta?style=social)

- `logo`
  Choose a logo from the [Simple Icons](https://simpleicons.org/) library and copy the "slug" by clicking the copy button in the corner of the logo's entry. The only drawback is that these are brand icons, so I chose the Gunicorn icon for the Ebena badge since it was the closest I could find to an Ebena Kuranto. Maybe you will want to use Apifox or Firefox for one of the Alsalto species, bunny.net for Salta Dentegos, Lubuntu, Fluentd, or LaTeX for bird-like species, Xubuntu for Maco Dornas,  PostgreSQL or Laragon for Pahidermos, SUSE for Koro degelas, or Docker for Nebulas. Spend some time looking through the icons, since brands are almost never named after the animal in their logo. Here's an example with Pyscaffold for Tagalos: ![Tagalo Count](https://img.shields.io/badge/Tagalo_count-200-magenta?logo=pyscaffold&style=for-the-badge)

- `logoColor`
   Can be a hex, rgb, rgba, hsl, hsla or css named colors. I use hex. This also affects the background of the right side of the badge. If you want that to be a different color than the logo, set the `color` parameter as well.
  
- `label`
  Self explanatory - whatever you want the label to say. I just use `Ebena%20count` for mine.

- `url`
    The magic part. Here is the url string with HTML escape characters:
  `https%3A%2F%2Ftfo.creaturetracker.net%2Fapi%2Fpublic%2Fusers%2Flyricism%2Fcreature-count%3Fspecies%3DEbena%2520Kuranto`
    - replace `lyricism` with your TFO username
    - replace `Ebena%2520Kuranto` with your chosen species, making sure if it is two words that both are capitalized and `%2520` is between them
      
## Putting it all together
The full markdown for the badge looks like this, I have put the parts you can or need to change in curly braces:

`![{Ebena count}](https://img.shields.io/endpoint?style={for-the-badge}&logo={gunicorn}&label={Ebena%20count}&url=https%3A%2F%2Ftfo.creaturetracker.net%2Fapi%2Fpublic%2Fusers%2F{lyricism}%2Fcreature-count%3Fspecies%3D{Ebena%2520Kuranto}&logoColor={D0BCFF})`

That's it! If you'd like to support what I'm doing, you can <a href="https://ko-fi.com/lyricism_">buy me a coffee</a> or become a patron on the <a href="https://patreon.com/tfoct?utm_medium=unknown&utm_source=join_link&utm_campaign=creatorshare_creator&utm_content=copyLink">tfoct Patreon</a>. Check out the [main tfoct repo](https://github.com/rio-codes/tfo-creaturetracker) for way more info!
