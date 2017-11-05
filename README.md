# Extend the implementation of AQM Evaluation Suite in ns-3

## Course Code: CO300

## Assignment: #19

### Overview

AQM Evaluation Suite [1] has been designed and developed at NITK Surathkal for ns-3 [2], based on recommendations of RFC 7928 [3]. This repository contains an extension of the given implementation with additional features crucial for evaluating AQM algorithms. 

The additional features included are: 
(1) `RemoveAqm` method to remove an AQM from the AQM list and
(2) Support of Byte Queue Limits (BQL).

### Example: using RemoveAqm method

To remove any specific AQM from the list (e.g., CoDel), use the following in `main ()` method of `aqm-eval-suite-runner.cc`:

` RemoveAqm ("CoDel"); `

### Example: Enable/Disable Byte Queue Limits (BQL)

To enable BQL for a particular scenario (e.g., AggressiveTransportSender), the command is:

`./waf --run "aqm-eval-suite-runner --name=AggressiveTransportSender --isBql=true"`

To run all scenarios at once with BQL enabled, the command is:

`./waf --run "aqm-eval-suite-runner --name=All --isBql=true"`

### References

[1] Deepak, A., Shravya, K. S., & Tahiliani, M. P. (2017, June). Design and Implementation of AQM Evaluation Suite for ns-3. In Proceedings of the Workshop on ns-3 (pp. 87-94). ACM.

[2] http://www.nsnam.org/

[3] Natarajan, P., Khademi, N., Kuhn, N., & Ros, D. (2016). Characterization Guidelines for Active Queue Management (AQM). Traffic, 1009, 28.
