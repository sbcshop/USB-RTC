# USB-RTC
USB RTC is an open source real time clock device that comprises MCP2221, a USB-to-UART/I2C serial converter, which enables USB connectivity, in the processes that include a USB, UART(Serial), GPIO, and I2C interfaces. 

### Installation on Raspberry Pi

* Install MCP2221 Library by running below command on terminal:

``` sudo pip3 install PyMCP2221A ```
              
* Connect USB-RTC on USB Port of Raspberry Pi.
* Now clone/download USB-RTC Github Repository by running below command:

```git clone https://github.com/sbcshop/USB-RTC.git ```

* Now enter downloaded folder from home/pi or by running below command:

``` cd USB-RTC ```

* Now run test.py file by running below command:

```sudo python3 test.py ```

### Installation on Windows

* Install MCP2221 Library by running below command on terminal:

``` pip install PyMCP2221A ```
              
* Connect USB-RTC on USB Port of Windows USB Port.
* 
* Now clone/download USB-RTC Github Repository by running below command:

```git clone https://github.com/sbcshop/USB-RTC.git ```

* Now enter downloaded folder.


* Now open and run test.py file by running below command:

```python3 test.py ``` or directly run test.py in any python supported ide.

### Functions

* To modify Date & Time, you have to change the last value of each line in hexadecimal form inside ```def SetTime(address):```

For Example : ``` bus.write_byte_data(0x68, 0x00, 0x02) # set seconds and start clock ``` , it will set second value as 02 second after executing  ```SetTime(address) ``` function.

* To read time , you can call ```ReadTime(address)``` Function
* To read internal temperature of USB-RTC, uncomment below line by removing ''' from start and end of the line :

    ```python Celsius = getTemp(address)
       Fahrenheit = 9.0/5.0 * Celsius + 32
       print (Fahrenheit, "*F /", Celsius, "*C") 
