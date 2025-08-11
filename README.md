
# walmart-convert-barcode

This nifty piece of code takes the little barcode under the TC number on a Walmart receipt and converts it to the TC number. Alternatively, it takes the TC number and converts it to the barcode. 

The barcode data is not the TC number itself, which poses a challenge for anyone trying to scan a TC number into a spreadsheet, or to generate barcodes based on already-stored TC numbers.




## Usage/Examples

Convert from the barcode to the TC number:
```python
from walmart_convert_barcode import getTC

barcodeData = "G$XCMEQE8$/AOH/D"
# this is an example of what scanning a barcode will yield
# it will always be 16 characters

tcNumber = getTC(barcodeData)   # input must be 16-digit str
# returns '1154123136508830806387'
```

Convert the TC number to a barcode:
```python
from walmart_convert_barcode import getBarcode

tcNumber = "3375305354916651614568"
# this is an example of a real-life TC number - these vary in length

barcodeData = getBarcode(tcNumber)  # input must be str
# returns 'G$YP4MK/C6J338NM'
```
