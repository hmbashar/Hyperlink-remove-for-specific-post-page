## Hyperlink remove for specific posts or pages

```
// Hyperlink remove for 5 posts
function atag_link_remove_here() {
	if(is_single(array(1604,2047,1827,1797,1534))) : // post/page id here which posts or pages do you want to remove anchor tag/link
	?>
		<script>
      // Content wrapper class
			jQuery('.thrv_wrapper').find('a').replaceWith(function(){
			return jQuery('<span/>', { // replace with span
				html: this.innerHTML
			});
		});

		</script>

<?php 
	endif;
}

add_action('wp_footer', 'atag_link_remove_here');
```
