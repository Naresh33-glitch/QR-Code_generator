# QR code generator using Python
This script take a link of any URL and generate a `QR code` corresponding to it.
### Prerequisites
`Python 3`
### Library Used
* [qrcode](https://github.com/lincolnloop/python-qrcode)

### To install required external modules
Run `pip install qrcode` 

### How to run the script
- Provide your desired URL in the script
- Execute `python3 QR_code_generator.py`

### Screenshot showing the sample use of the script
import qrcode

input_URL = "https://www.google.com/"

qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_L,
    box_size=15,
    image_size=20,
    border=0,
)

qr.add_data(input_URL)
qr.make(fit=True)

img = qr.make_image(fill_color="Blue", back_color="White")
img.save("url_qrcode.png")

print(qr.data_list)
### Output
<img width="375" height="375" alt="url_qrcode" src="https://github.com/user-attachments/assets/27f31b38-b838-4144-921a-89b16c503513" />


## *Author Name*
Naresh S
212224240101
