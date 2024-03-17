<script>
    import { Body } from 'svelte-body';
    const style = {
        color: 'green',
        '--cool-css-prop': '😎'
    };

    import { page } from '$app/stores';
    let path;

    $: path = $page.url.pathname;

</script>


<Body {style} />

<div class='plantas'> 
  <h1 style="font-size:11vw">¡Plantas Patraldo!</h1>
<p>La Plantera Rosa</p>
</div>

<div class='email'>
<h1 style="font-size:7vw;"><a href = "mailto:infoplantas@patraldo.com">Email</a></h1>
</div>

<iframe width="600" height="450" style="border:0" Loading="lazy" allowfullscreen src="https://www.google.com/maps/embed/v1/place?q=place_id:ChIJO-etgvyvKIQRbqwoDvNUPJA&key=AIzaSyDSFnLS3cxT4yHYxcKqf5pXxg6C_OCoVH0"></iframe>

<style>
@import url('https://fonts.googleapis.com/css2?family=Bungee+Spice&family=Pacifico&family=Special+Elite&family=Tangerine:wght@400;700&family=Ultra&display=swap');


@keyframes move-bg {
  to {
    background-position: var(--bg-size) 0;
  }
}

/* https://web.dev/speedy-css-tip-animated-gradient-text/ */
.plantas {
  --bg-size: 400%;
  --color-one: hsl(7 85% 43%);
  --color-two: hsl(50 95% 73%);
  --color-three: hsl(318 94% 7%);
  background-clip: padding-box;
font-family: 'Special Elite';
margin: 10px;
padding: 10px;
text-align: center;

background: linear-gradient(
                90deg,
                var(--color-one),
                var(--color-two),
                var(--color-three)
              ) 0 0 / var(--bg-size) 100%;
  color: transparent;
  -webkit-background-clip: text;
  background-clip: text;
  animation: move-bg 8s infinite linear;
}

.plantas p {
  --bg-size: 200%;
  --color-one: hsl(7 85% 43%);
  --color-two: hsl(50 95% 73%);
  --color-three: hsl(318 94% 7%);
  background-clip: padding-box;
font-family: 'Special Elite';
margin: 10px;
padding: 10px;
text-align: center;
}



iframe {
width: 100%;
aspect-ration: 16/9;
}

a, a:hover, a:active, a:visited, a:focus {
color: black;
    text-decoration:none;
}

.email {
border: 10px dotted black;
 background: goldenrod;
 background-clip: padding-box;
font-family: 'Special Elite';
margin: 10px;
padding: 10px;
text-align: center;
color: black;
}

.email a:hover {
color: green;
}



</style>


