# ACPI 
Most of the SSDTs in this folder are created using SSDTTime, with the exception of SSDT-PLUG (it is prebuilt) and SSDT-dGPU-Off.

### SSDT-dGPU-Off
* Created using the following guide: [Disabling laptop dGPUs (SSDT-dGPU-Off/NoHybGfx)  (Optimus Method)](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/laptop-disable.html#optimus-method)

	```swift
	DefinitionBlock ("", "SSDT", 2, "DRTNIA", "dGPU-Off", 0x00000000)
	{
    	External (_SB_.PCI0.RP01.PEGP._OFF, MethodObj)    // 0 Arguments

    	Device (RMD1)
    	{
        	Name (_HID, "RMD10000")  // _HID: Hardware ID
        	Method (_STA, 0, NotSerialized)  // _STA: Status
        	{
            	If (_OSI ("Darwin"))
            	{
                	Return (0x0F)
            	}
            	Else
            	{
                	Return (Zero)
            	}
        	}

        	Method (_INI, 0, NotSerialized)  // _INI: Initialize
        	{
            	If (_OSI ("Darwin"))
            	{
                	If (CondRefOf (\_SB.PCI0.RP01.PEGP._OFF))
                	{
                    	\_SB.PCI0.RP01.PEGP._OFF ()
                	}
            	}
            	Else
            	{
            	}
        	}
    	}
	}
	```