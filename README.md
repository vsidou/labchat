# labchat
### A set of modules for communicating with some common scientific laboratory equipment

The project currently includes 5 modules for working with 5 different pieces of common laboratory equipment.  All modules use Python's built-in `logging` module for feedback.  Each module defines its own logger with the same name as the pakcage using `logger = logging.getLogger(__name__)`.

## The modules

  1. **`bkprecision`**: For working with function generators made by [BK Precision](http://www.bkprecision.com/products/signal-generators.html).  The module was specifically developed for working with the 4050 series signal generators but should work with many of their other products as well.  It relies on the [`pyvisa` package](https://github.com/hgrecco/pyvisa) for communication.
  2. **`ncdrelay`**: A small module for controlling RS-232 controllable relays produced by [National Control Devices](https://www.controlanything.com/Relay/Relay/RS232_Relay_Controllers).  It relies on the [`pyvisa` package](https://github.com/hgrecco/pyvisa) for communication. 
  3. **`ophirpower`**: A package for communicating with [Ophir power meters](http://www.ophiropt.com/laser--measurement/products/Laser-Power-Meters-Laser-Energy-Meters) which are commonly found in optical labs.  The package was tested on the Vega series of power meter heads, but should be compatible with other Ophir power meter heads as well.  It relies on the [`win32com` package](https://sourceforge.net/projects/pywin32/files/pywin32/) for communication.
  4. **`tekscope`**: A module for communicating with [Tektronix oscilloscopes](http://www.tek.com/oscilloscope).  The module was designed for and tested on the TDS and DPO series oscilloscopes.  The oscilloscopes have hundreds of commands and only the most common are implemented as class methods so it will be necessary to look up the programmer's manual from Tektronix in order to access all features of the scope.  This package relies on the [`pyvisa` package](https://github.com/hgrecco/pyvisa) for communication.
  5. **`edgetech`**: A module for communicating with [Edgetech Instruments](http://www.edgetechinstruments.com/) hygrometers.  The module is specifically designed to communicate with their DewMaster chilled mirror hygrometer system.  It relies on the [`pyvisa` package](https://github.com/hgrecco/pyvisa) for communication.
  6. **`gwinstek`**: A module for communicating with devices manufactured by [GW Instek](http://www.gwinstek.com/).  It currently includes a class for controlling their [AFG-2225 arbitrary waveform generator](http://www.gwinstek.com/en-global/products/Signal_Sources/Arbitrary_Function_Generators/AFG-2225).  It relies on the [`pyvisa` package](https://github.com/hgrecco/pyvisa) for communication.
