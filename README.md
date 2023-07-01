import TesseractOCR

func performOCR(on image: UIImage) {
    if let tesseract = G8Tesseract(language: "jpn") {
        tesseract.image = image.g8_blackAndWhite()
        tesseract.recognize()

        let recognizedText = tesseract.recognizedText
        print(recognizedText)
    }
}
