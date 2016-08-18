#InvoiceFox Superfolder

Get ID of document based on document number. First one is for invoices, second for estimates and proformas.

    ./get-id invoice-sent 00020/2014

    ./get-id preinvoice P14-0001

Downloads invoice PDF-s with id-s from 100 to 110 (inclusive). In second case download estimates or pro-forma invoices.

    ./download invoice-sent 100 110 pdf

    ./download preinvoice 1 15 pdf

Prints first 10 PDF-s in local folder. Withouth "go" it just displays which it will print.

    ./print-some 1 10 #lists first 10 PDF-s

    ./print-some 1 10 go #sends first 10 PDF-s to printer

##Setup

###.invfox-api-token

You have two setup files. One holds just the API token. Rename .invfox-api-token-SAMPLE to .invfox-api-token 
and copy in your API token. Make the file unreadable by group and other.

###print.cfg

Config file for print command. It has 2 settings: virtual name of your printer (you can create a specific name with 
specific settings and then use it here, at least on Linux). And media type, for example A4 or Letter.

    printer:Samsung-color
    media:A4

###download.cfg

Config file for download command.

    domain:www.cebelca.biz
    lang:si
    doctitle:Račun%20št.

##Commands

    $ ./get-id invoice-sent "14-0005"  # get's the id of invoice based on a invoice number
    $ ./get-id invoice-sent "14-0025"  

    $ ./download <resource> <idStart> <idEnd> pdf # downloads invoices between ID-s

    $ ./print-some 1 10 # shows which pdfs it would sent do print (first 10)
    $ ./print-some 1 10 go # sends first 10 pdfs to print

    $ ./clrpdfs # deletes all the pdfs in the folder
    $ ./cntpdfs # counts the pdfs

##State

Works, we use it ouserlves for http://www.cebelca.biz and http://www.invoicefox.com

##Plan

 * to add functionality where you get invoice ID-s based on date or Invoice Number
 * ideas welcome
