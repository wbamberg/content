---
title: Barcode Detection API
slug: Web/API/Barcode_Detection_API
tags:
  - API
  - Landing
  - Overview
  - barcode
  - barcode detection
  - shape detection
---
{{draft}}{{securecontext_header}}{{DefaultAPISidebar("Barcode Detection API")}} {{AvailableInWorkers}}

The Barcode Detection API detects linear and two-dimensional barcodes in images.

## Concepts and usage

Support for barcode recognition within web apps unlocks a variety of use cases through supported barcode formats. QR codes can be used for online payments, web navigation or establishing social media connections, aztec codes can be used to scan boarding passes and shopping apps can use EAN or UPC barcodes to compare prices of physical items.

Detection is achieved through the {{domxref('BarcodeDetector.detect()','detect()')}} method, which takes an image object; either an {{HTMLElement('img', ' element')}}, a {{domxref('Blob')}}, {{domxref('ImageData')}} or a {{domxref('CanvasImageSource')}}. Optional parameters can be passed to the {{domxref('BarcodeDetector')}} constructor to provide hints on which barcode formats to detect.

### Supported barcode formats

The Barcode Detection API supports the following barcode formats:

| Format      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Image                                                                                                               |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| aztec       | A square two-dimensional matrix following iso24778 and with a square bullseye pattern at their centre, thus resembling an Aztec pyramid. Does not require a surrounding blank zone.                                                                                                                                                                                                                                                                                    | ![A sample image of an aztec barcode. A square with smaller black and white squares inside](aztec.gif)              |
| code_128    | A linear (one-dimensional), bidirectionally-decodable, self-checking barcode following iso15417 and able to encode all 128 characters of ASCII (hence the naming).                                                                                                                                                                                                                                                                                                     | ![An image of a code-128 barcode. A horizontal distribution of vertical black and white lines](code-128.gif)        |
| code_39     | A linear (one-dimensional), self-checking barcode following iso16388. It is a discrete and variable-length barcode type.                                                                                                                                                                                                                                                                                                                                               | ![An image of a code-39 barcode. A horizontal distribution of vertical black and white lines](code-39.png)          |
| code_93     | A linear, continuous symbology with a variable length following bc5. It offers a larger information density than Code 128 and the visually similar Code 39. Code 93 is used primarily by Canada Post to encode supplementary delivery information.                                                                                                                                                                                                                     | ![An image of a code 93 format barcode. A horizontal distribution of white and black horizontal lines](code-93.png) |
| codabar     | A linear barcode representing characters 0-9, A-D and symbols - . $ / +                                                                                                                                                                                                                                                                                                                                                                                                | ![An image of a codabar format barcode. A horizontal distribution of black and white vertical lines](codabar.png)   |
| data_matrix | An orientation-independent two-dimensional barcode composed of black and white modules arranged in either a square or rectangular pattern following iso16022.                                                                                                                                                                                                                                                                                                          | ![An example of a data matrix barcode. A square filled with smaller black and white squares](data-matrix.png)       |
| ean_13      | A linear barcode based on the UPC-A standard and defined in iso15420.                                                                                                                                                                                                                                                                                                                                                                                                  | ![An image of an EAN-13 format barcode. A horizontal distribution of white and black lines](ean-13.png)             |
| ean_8       | A linear barcode defined in iso15420 and derived from EAN-13.                                                                                                                                                                                                                                                                                                                                                                                                          | ![An image of an EAN-8 format barcode. A horizontal distribution of vertical black and white lines](ean-8.png)      |
| itf         | A continuous, self-checking, bidirectionally decodable barcode. It will always encode 14 digits.                                                                                                                                                                                                                                                                                                                                                                       | ![An image of an ITF Barcode. A horizontal distribution of white and black lines](ift.png)                          |
| pdf417      | A continuous two-dimensional barcode symbology format with multiple rows and columns. It's bi-directionally decodable and uses the iso15438 standard.                                                                                                                                                                                                                                                                                                                  | ![An example of a pdf417 barcode format. A rectangle of smaller black and white squares](pdf417.png)                |
| qr_code     | A two-dimensional barcode that uses the iso18004 standard. The information encoded can be text, URL or other data.                                                                                                                                                                                                                                                                                                                                                     | ![An example of a QR code. A square of smaller black and white squares](qr-code.png)                                |
| upc_a       | One of the most common linear barcode types and is widely applied to retail in the United States. Defined in iso15420, it represents digits by strips of bars and spaces, each digit being associated to a unique pattern of 2 bars and 2 spaces, both of variable width. UPC-A can encode 12 digits that are uniquely assigned to each trade item, and it’s technically a subset of EAN-13 (UPC-A codes are represented in EAN-13 with the first character set to 0). | ![An image of a upc-a barcode. A rectangle of black and white vertical lines with numbers underneath](upc-a.png)    |
| upc_e       | A variation of UPC-A defined in iso15420, compressing out unnecessary zeros for a more compact barcode.                                                                                                                                                                                                                                                                                                                                                                | ![An image of a upc-e barcode. A rectangle of black and white vertical lines](upc-e.png)                            |
| unknown     | This value is used by the platform to signify that it does not know or specify which barcode format is being detected or supported.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                     |

You can check for formats supported by the user agent via the {{domxref('BarcodeDetector.getSupportedFormats()','getSupportedFormats()')}} method.

## Interfaces

- {{domxref("BarcodeDetector")}}
  - : The **`BarcodeDetector`** interface of the Barcode Detection API allows detection of linear and two dimensional barcodes in images.

## Examples

### Creating A Detector

This example tests for browser compatibility and creates a new barcode detector object, with specified supported formats.

```js
// check compatibility
if (!('BarcodeDetector' in window)) {
  console.log('Barcode Detector is not supported by this browser.');
} else {
  console.log('Barcode Detector supported!');

  // create new detector
  var barcodeDetector = new BarcodeDetector({formats: ['code_39', 'codabar', 'ean_13']});
}
```

### Getting Supported Formats

The following example calls the `getSupportFormat()` method and logs the results to the console.

```js
// check supported types
BarcodeDetector.getSupportedFormats()
  .then(supportedFormats => {
    supportedFormats.forEach(format => console.log(format));
  });
```

### Detect Barcodes

This example uses the `detect()` method to detect the barcodes within the given image. These are iterated over and the barcode data is logged to the console.

```js
  barcodeDetector.detect(imageEl)
    .then(barcodes => {
      barcodes.forEach(barcode => console.log(barcode.rawData));
    })
    .catch(err => {
      console.log(err);
    })
```

## Specifications

| Specification                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------- |
| [Accelerated Shape Detection in Images # barcode-detection-api](https://wicg.github.io/shape-detection-api/#barcode-detection-api) |

## Browser compatibility

{{Compat("api.BarcodeDetector")}}

## See also

- [barcodefaq.com: A website with information about different barcodes and examples of the different types.](https://www.barcodefaq.com/)
- [The Shape Detection API: a picture is worth a thousand words, faces, and barcodes](https://web.dev/shape-detection/#barcodedetector)
