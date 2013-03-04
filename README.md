#InvoiceFox Superfolder

Downloads invoice PDF-s with id-s from 100 to 110 (inclusive). Formats can be pdf, odt and doc.

    ./download 100 110 pdf

Prints first 10 PDF-s in local folder. Withouth "go" it just displays which it will print.

    ./print-some 1 10 #lists first 10 PDF-s

    ./print-some 1 10 go #sends first 10 PDF-s to printer

#Setup

##.invfox-api-token

You have two setup files. One holds just the API token. Rename .invfox-api-token-SAMPLE to .invfox-api-token 
and copy in your API token. Make the file unreadable by group and other.

##print.cfg

Config file for print command. It has 2 settings: virtual name of your printer (you can create a specific name with 
specific settings and then use it here, at least on Linux). And media type, for example A4 or Letter.

    printer:Samsung-color
    media:A4

##download.cfg

Config gile for download command.

    domain:www.cebelca.biz
    lang:si
    doctitle:Račun%20št.

##State

Works.

##Plan

 * to add functionality where you get invoice ID-s based on date or Invoice Number
 * ideas welcome
