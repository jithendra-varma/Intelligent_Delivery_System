# **Programming specific tasks for NFC**

NFC is a set of short-range wireless technologies, typically requiring a separation of 10 cm or less. NFC operates at 13.56 MHz on ISO/IEC 18000-3 air interface and at rates ranging from 106 kbit/s to 424 kbit/s. NFC always involves an initiator and a target; the initiator actively generates an RF field that can power a passive target. This enables NFC targets to take very simple form factors such as unpowered tags, stickers, key fobs, or cards. NFC peer-to-peer communication is possible, provided both devices are powered. 

NFC tags contain data and are typically read-only, but may be writable. They can be custom-encoded by their manufacturers or use NFC Forum specifications. The tags can securely store personal data such as debit and credit card information, loyalty program data, PINs and networking contacts, among other information. The NFC Forum defines four types of tags that provide different communication speeds and capabilities in terms of reconfigurability, memory, security, data retention and write endurance.

![NFC](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.012.jpeg)

As with proximity card technology, NFC uses inductive coupling between two nearby loop antennas effectively forming an air-core transformer. Because the distances involved are tiny compared to the wavelength of electromagnetic radiation (radio waves) of that frequency (about 22 meters), the interaction is described as a near field. Only an alternating magnetic field is involved so that almost no power is actually radiated in the form of radio waves (which are electromagnetic waves, also involving an oscillating electric field); that essentially prevents interference between such devices and any radio communications at the same frequency or with other NFC devices much beyond its intended range. They operate within the globally available and unlicensed radio frequency ISM band of 13.56 MHz. Most of the RF energy is concentrated in the ±7 kHz bandwidth allocated for that band, but the emission's spectral width can be as wide as 1.8 MHz in order to support high data rates.

NFC allows you to share small payloads of data between an NFC tag and an Android-powered device, or between two Android-powered devices. The data stored in the tag can also be written in a variety of formats, but many of the Android framework APIs are based around an NFC Forum standard called NDEF (NFC Data Exchange Format).

Android-powered devices with NFC simultaneously support three main modes of operation:

1. **Reader/writer mode**, allowing the NFC device to read and/or write passive NFC tags and stickers.
2. **P2P mode**, allows the NFC device to exchange data with other NFC peers; this operation mode is used by Android Beam.
3. **Card emulation mode**, allowing the NFC device itself to act as an NFC card. The emulated NFC card can then be accessed by an external NFC reader, such as an NFC point-of-sale terminal.

In our system, we are using P2P mode to transfer the information between NFC peers that is the customer and retailer. The following are the steps involved in writing specific information onto the tag.

## Getting a tag

We bought the following NFC tag for the delivery system based on the specifications and requirements (RapidRadio 13.56 MHz ISO 14443A: NFC Type 2 NTAG213 HF RFID NFC NTag Sticker)

Specifications:

- Operating Frequency: 13.56 MHz High Frequency (HF)
- Material: Label
- Standards/Protocols: ISO 14443A : NFC Type 2
- Integrated Circuit: NTAG213
- Applications: Payments | Wireless Pairing | Access Control | Customer Loyalty.

## Install an NFC Tag writer app

There are a number of free apps that can write NFC tags on Google Play. A few are Trigger, NFC Tools, and NFC TagWriter by NXP. We are using the NFC tools app for writing the NDEF encoding onto the NFC chip.

![Program NFC chip NFC Tools app](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.013.jpeg)

## Open the NFC Tools app

After opening the app, you will be greeted with this home page. Click "Write" to move on to the next step. 

![NFC Tools app coding an NFC Tag](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.014.jpeg)

## Add a record

Here, you will see a page with three options. Click the first option, **"Add A Record,"** to move on to step 5.

![NFC tools Tap Tag](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.015.jpeg)

## Adding the required records

This step greets you with many options to code into your Tap Tag. The recommended option is to click **"Custom URL/URI."** Move on to the next step.

![NFC chip capabilities](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.016.jpeg)

## Adding the custom URL

After clicking **"Custom URL/URI",** the app will bring you to this simple page. Just type in your www. or copy/paste your web link. Click **"OK"** in the top right corner when you are done.

![NFC Tools Add link to NFC tag](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.017.jpeg)

## Writing the information onto the tag

After clicking **"OK",** you will be brought back to this page. This time your Custom URL will be added. You will also notice the app tells you the amount of space your link takes up, in this case, 16 Bytes. Click **"Write"** to be prompted with an NFC **"Ready to Scan"** message.

![Program a link into NFC chip](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.018.jpeg)

## Scanning the tag

Now your smartphone is looking for an NFC tag to encode. For iPhone, hold the top of your phone within 1 inch of Tap Tag while this message is up. For android, place the middle of the phone onto Tap Tag.  Your smartphone will make a sound and/or vibrate when your NFC tag is officially encoded, which takes less than one second. 

![Ready to scan NFC tag - Coding](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.019.jpeg)

## Finishing the task

This checkmark symbolizes that your NFC chip is programmed! 

![NFC App to code NFC tag](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.020.jpeg)

## NFC Tag Position

That is how we programmed the NFC tag to perform all the tasks. For our delivery system, we used four NFC Tags each one having different functionalities.

- Product Information
- Payment 
- Contact Information
- Customer Loyalty Program

These tags are placed behind their respective pictures each describing the content of the NFC tag behind them.

![](Aspose.Words.c332127a-1b76-4b79-b803-9d6ae9d207a1.021.png)
