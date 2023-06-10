# fzCrack
Did you create a ZIP archive with password protection, but forgot to take note? Can happen, we are humans!
Even you forgot the password or for some reason yo want to crack the password, you are in the right place.

This tool is based on the project zzCrack, but that implementation is single thread.
It was added the support to start multiple process in order to reach the goal faster.

The tool could load a word dictionary or can use the brute force approach to unlock the ZIP archive.

## Download
You can clone this repo or simply download the fz.py and manually install the requirements.

## Usage
```
python fz.py --help
```

## Examples
Word dictionary and stream to stout the complete output of the process
```
python fz.py -f test.zip -w rockyou.txt --stream
```

Brute force with all charset (0-9,a-z,symbols all cases) and stream to stout the complete output of the process (single thread)
```
python fz.py -f test.zip -b -c 0+2 --stream
```

Parallel processing using brute force approach (start the processes in separated command prompt or use Terminator with splitted windows)
```
python fz.py -f test.zip -b -c 0+2 --min-lenght 1 --max-lenght 4 --stream
python fz.py -f test.zip -b -c 0+2 --min-lenght 5 --max-lenght 6 --stream
python fz.py -f test.zip -b -c 0+2 --min-lenght 6 --max-lenght 7 --stream
python fz.py -f test.zip -b -c 0+2 --min-lenght 7 --max-lenght 8 --stream
```
