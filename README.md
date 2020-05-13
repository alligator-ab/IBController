# IBController
IBController 1.3.8 fork. Provides a COM interface for an easy access to Interactive Brokers TWS API.

IBController is AmiBroker Auto-Trading interface for Interactive Brokers. Developed by Tomasz Janesko up to version 1.3.8, this repository hosts a fork. See https://www.amibroker.com/at/ (note that this project is in no way related to https://github.com/ib-controller/ )

License
=======
IBController source code is licensed under Creative Commons Attribution-ShareAlike 3.0 Unported  (CC BY-SA 3.0) License.
https://creativecommons.org/licenses/by/3.0/

Disclaimer
==========
AMIBROKER.COM, AUTHORS AND CONTRIBUTORS MAKE NO REPRESENTATION 
ABOUT THE SUITABILITY OF THIS SOURCE CODE FOR ANY PURPOSE. 
IT IS PROVIDED "AS IS" WITHOUT EXPRESS OR IMPLIED WARRANTY OF ANY KIND. 
AMIBROKER.COM DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOURCE CODE, 
INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. 
IN NO EVENT SHALL AMIBROKER.COM BE LIABLE FOR ANY SPECIAL, INDIRECT, INCIDENTAL, OR 
CONSEQUENTIAL DAMAGES, OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, 
WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, 
ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOURCE CODE.

Help
====
IBController is an independant program from Amibroker but as most users are Amibroker's, you can seek help on
https://forum.amibroker.com/ (discourse forum) in section 'IBController'.

Contribution
============
Contributions are welcome. See above.

Bug report
==========
The current maintainer of this project is member's forum 'alligator'. Send a PM to report bugs or ask for features.
Contributors are welcome.


Comparison with version 1.3.8
=============================
Bugs fixed:
----------
- precision was insuficient to place orders at every tick for a number of instruments notably treasury futures and currency pairs. Fixed.

Interface improvements:
----------------------
- new tabs, in particular Orders, to keep note of every trade placed, and P&L, for an easy access to performance
- better organization of messages in Messages tab
- alternate colored rows 

API additions:
-------------
- GetOrdersList(Field, Filter) retrieve a comma-separated list of field from the Orders tab, matching Filter ("" for all) 
- GetOrderInfo(OrderID, Field) specific value of field Field for order OrderID (a number)
- placeOrderEx("...") place an order using JSON-like syntax, all fields from Order struct type can be accessed (after api upgrade)


Roadmap
=======
- code modernization
	CString replaced by std::string
- cleaning
- Upgrade to TWS API 979.1
- Addition of various APIs: 
	* real-time depth of market, 
	* News, 
	* Option greeks, 
	* Fundamentals (reuters)
- RESTful API to invoke IBController


