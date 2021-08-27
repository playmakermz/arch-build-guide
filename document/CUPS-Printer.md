# Install Printer using cups

Install Driver Printer using CUPS, This method is work with TS307, i think this work with others 
(Dymo Label Printer, EPSON, HP, And etc) for more information <https://github.com/apple/cups>

1. ``` sudo pacman -S cups cups-pdf ```
1. ```systemctl list-unit-files | grep 'cups' # optional, enable every cups system ```
1. ``` sudo systemctl restart cups; sudo systemctl start cups ;sudo systemctl enable cups ```
1. ``` sudo pacman -S print-manager # install GUI application printer```
1. Using website for printer <http://localhost:631/admin>
##### Refrensi
<https://askubuntu.com/questions/547131/kde-5-plasma-printer-configuration-module-not-found> <br>
<https://gist.github.com/notdodo/660a2a67b9bc8a815ba537530137636a>
