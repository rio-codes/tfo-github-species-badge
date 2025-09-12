# tfo-github-species-badge
A shields.io Github profile badge that counts members of a given species in your collection on [tfo.creaturetracker.net](https://tfo.creaturetracker.net), a breeding tracker for [The Final Outpost](https://finaloutpost.net)


## The Badge

![Ebena count](https://img.shields.io/endpoint?style=for-the-badge&logo=gunicorn&label=Ebena%20count&url=https%3A%2F%2Ftfo.creaturetracker.net%2Fapi%2Fpublic%2Fusers%2Flyricism%2Fcreature-count%3Fspecies%3DEbena%2BKuranto%26color%3DD0BCFF&logoColor=D0BCFF)

Yup. That many horses. Look at this weird one:<br />
![https://finaloutpost.net/view/WoZK6/](https://finaloutpost.net/rimg/WoZK6.png)

## Needed Info

<b>NOTE:</b> You need to have an account on [tfoct](https://tfo.creaturetracker.net) to use this utility. If you don't have one, check our our <a href="https://patreon.com/tfoct?utm_medium=unknown&utm_source=join_link&utm_campaign=creatorshare_creator&utm_content=copyLink">Patreon</a> for early access, or wait until the full public release on September 18th. If you are interested in helping us beta test our site, join our <a href="https://discord.gg/PMtE3jrXYR">Discord</a> and say hi! We don't bite, I promise.

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
   Can be a hex, rgb, rgba, hsl, hsla or css named colors. I use hex. For the the color on the right side of the badge, edit it in the URL query parameters below.
  
- `label`
  Self explanatory - whatever you want the label to say. I just use `Ebena%20count` for mine.

- `url`
    The magic part. Our api endpoint is `/api/public/users/{username}/creature-count?species={species}&color={color}` Here is the url string with HTML escape characters:
  `https%3A%2F%2Ftfo.creaturetracker.net%2Fapi%2Fpublic%2Fusers%2Flyricism%2Fcreature-count%3Fspecies%3DEbena%2BKuranto%26color%3DD0BCFF`
    - replace `lyricism` with your TFO username
    - replace `Ebena%2BKuranto` with your chosen species, making sure if it is two words that both are capitalized and `%2B` is between them
    - change `color` to a preferred color for the right side of the badge. It follows the rules shields.io has for colors, so hex, rgb, rgba, hsl, hsla or css named colors are allowed.
      
## Putting it all together
The full markdown for the badge that you will put into your Github README (or anywhere else on the web) looks like this, I have put the parts you can or need to change in curly braces:

`![{Ebena count}](https://img.shields.io/endpoint?style={for-the-badge}&logo={gunicorn}&label={Ebena%20count}&url=https%3A%2F%2Ftfo.creaturetracker.net%2Fapi%2Fpublic%2Fusers%2F{lyricism}%2Fcreature-count%3Fspecies%3D{Ebena%2BKuranto}%26{color%3DD0BCFF}&logoColor={D0BCFF})`

## Source code
Just for those who are curious, I have put the source for the creature-count API route in this repo as `route.ts`, but it is part of the <a href="https://github.com/rio-codes/tfo-creaturetracker">full tfoct project</a> so it won't help much on its own.
