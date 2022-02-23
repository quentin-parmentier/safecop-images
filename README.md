# safecop-images

## IMAGE
magick "$($i).png" -fuzz "2%" -transparent "#ffffff" "$($i).png"

$table=Get-ChildItem
foreach($row in $table) {magick "$($row.name)" -fuzz 2% -fill "#F0F0F0" -opaque "#ffffff" -strip -quality 69 -interlace JPEG -colorspace sRGB -sampling-factor 4:2:0 -resize 500x500 "$($row.Basename).jpg"}