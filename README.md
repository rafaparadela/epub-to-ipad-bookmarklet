epub-to-ipad-bookmarklet
========================

Bookmarklet for download epubs 

##How works

- Create a bookmark with this code

`javascript:var rating = jQuery('.rating>.post-ratings');var id = rating.attr('id');id=id.split('post-ratings-')[1];var link = jQuery('.social>a');if(link.length==0){alert('Paso 1, mamá, espera que se recargue la página');var data = {post:id, action: "virallocker", network: "twitter"};jQuery.post("http://todoepub.es/wp-admin/admin-ajax.php", data, function(response) {if (virallocker_use) location.reload();});}else{var url = link.attr('href');var social = link.parent();var form = jQuery('<form></form>').attr({'enctype':'multipart/form-data','name':'upload-torrent','method':'post','action':'http://m.zbigz.com/myfiles'});social.append(form);var input = jQuery('<input>').attr({'id':'text-link-input','name':'url','value':url}); form.append(input);form.submit();}`

- Go to todoepub.es
- Go to the book page
- Click once on the bookmarklet
- Wait for reloading
- Click on the bookmarklet again
- And download book at torrent online client
