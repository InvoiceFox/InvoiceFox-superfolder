#InvoiceFox Superfolder

Downloads invoice PDF-s with id-s from 100 to 110 (inclusive).

  ./download 100 110

Prints first 10 PDF-s in local folder. Withouth "go" it just displays which it will print.

  ./print-some 1 10 #lists first 10 PDF-s

  ./print-some 1 10 go #sends first 10 PDF-s to printer

#Setup

.invfox-api-token #insert your api token here, make it unreadable by group and other

print.cfg

  printer:Samsung-color
  media:A4


