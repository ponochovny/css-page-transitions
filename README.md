<img width="1222" height="716" alt="image" src="https://github.com/user-attachments/assets/70670a99-7cc5-4fd5-9e25-ea2237a910ab" />

``` CSS
@media (prefers-reduced-motion: no-preference) {...}

@view-transition {
	navigation: auto;
}

/* ::view-transition-group(root) { */
::view-transition-group(page-content) {
	animation-duration: 0.5s;
	animation-timing-function: ease;
}

/* ::view-transition-old(root) { */
::view-transition-old(page-content) {
	animation-name: slide-out;
}

/* ::view-transition-new(root) { */
::view-transition-new(page-content) {
	animation-name: slide-in;
}

main {
	view-transition-name: page-content;
}

.card img,
.hero-image {
	view-transition-name: article-image;
}

@keyframes slide-out {
	to {
		translate: -100vw;
	}
}
@keyframes slide-in {
	from {
		translate: 100vw;
	}
}
```
