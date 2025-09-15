# Jellyfin-BackgroundScroll
Add a slow scrolling effect to the Jellyfin Item page background

# Installation
Add code to you jellyfin custom css
```
@keyframes backgroundScroll {
    0% { transform: translate(-12%,0%); opacity: 0; }
    0.1% { opacity: 1; }
    10% { transform: translate(0%,-6%); }
    20% { transform: translate(-12%,0%); }
    30% { transform: translate(0%,-6%); }
    40% { transform: translate(-12%,0%); }
    50% { transform: translate(0%,-6%); }
    60% { transform: translate(-12%,0%); }
    70% { transform: translate(0%,-6%); }
    80% { transform: translate(-12%,0%); }
    90% { transform: translate(0%,-6%); }
	99.9% { opacity: 1; }
    100% { transform: translate(-12%,0%); }
}

.backdropImage {
   width: 125%;
   height: 125%;
   zoom: 125%;
   opacity:0 ;
   background-position: 99% 1%;
   animation: backgroundScroll 320s ease-in-out infinite;
}

.itemBackdrop {
   background-position: 99% 1%;
   opacity:0 ;
   animation: void 320s ease-in-out;
}

@keyframes void {
    0% { opacity: 0; }
    100% { opacity: 0; }
}
```
