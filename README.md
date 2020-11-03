# automatedSpinCoater
This project is for automating a Laurel Technologies Spin Coater for use in fabrication of polyamide Reverse Osmosis Membranes

The LabView 2018 folder contains the following files:

"basic_serial_write_and_read.vi"
"Control Pumps (SubVI).vi"
"Send SMS simplified.vi"
"Spin Coar ReadStops(SubVI).vi"
"Spin Coat LbL Krizak SMS.vi"

and
"NE-1000_20Syringe_20Pump_20LabView_20Driver_20VIs"
which contains "Stop Pups (SubVI).vi"

The main program is the "Spin Coat LbL Krizak SMS.vi"
This programs utilizes the SubVI's to operate

The program starts by reading the given COM port for the spin coater to detect once the device has stopped spinning.
This will then direct the pump to deposit a set volume of solution for the given rate, and then infuse a few fractions of milliliter to prevent dripping solution on the support in between depositions.
The program will then wait a preset amount of time to begin reading the spin coater again
The pumps will operate in sequence 0 to 4 or 0 to 5, depending on whether an additional pump is required.
The sequence will repeat until the number of layers specified have been completed.
A text message will be sent on the second to last layer as a reminder that the process is nearing completion and a final reminder when complete.

This work was modeled after the article:
Chan, E., Lee, J., Chung, J., Stafford, C. (2012). An automated spin-assisted approach for molecular layer-by-layer assembly of crosslinked polymer thin films. The Review of scientific instruments  83(11), 114102. https://dx.doi.org/10.1063/1.4767289
