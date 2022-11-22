# sunmi_printer_ticket

 # This is a fork from [sunmi_printer](https://pub.dev/packages/sunmi_printer) , but i implemented a lot of other features described below
 # Important: 
  **THIS PACKAGE WILL WORK ONLY IN ANDROID!**
  - [x] Jump (n) lines
  - [x] Bold mode on/off
  - [x] Cut paper - Dedicated method just to cut the line
## Tested Devices

Sunmi V2 Pro 

## import packages
   import '../service_printer_pos/sunmi_printer.dart';
// all method from sunmi printer need to async await

 await SunmiPrinter.startPrinter(); // start printer
 ```
## Example code when use for transaction printing
    await SunmiPrinter.startPrinter();
    await SunmiPrinter.printText(text: AppConst.nameCompany, bold: true, size: 20);
    await SunmiPrinter.printText(text: "${AppConst.taxCodeName} ${AppConst.taxCodeCustomer}", bold: false, size: 20); // size =20 : font size printer
    await SunmiPrinter.setAlignment(1); // 0 : Left align , 1 : Center align, 2 : Right align
    await SunmiPrinter.printLine(3); // Jump (3) lines
    await SunmiPrinter.cutPaper(); // Dedicated method just to cut the line
 
