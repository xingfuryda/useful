useful
======

bat file for downloading videos:

cd downloaded
move *.mp4 ..\archive
cd ..

wget -O videos.txt --no-check-certificate http://immense-thicket-5879.herokuapp.com/

for /F "tokens=*" %%A in (videos.txt) do youtube-dl %%A -f 18/22 --max-filesize 100m --download-archive complete.txt

move *.mp4 downloaded
