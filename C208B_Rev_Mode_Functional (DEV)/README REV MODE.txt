The PFD and MFD behavior during start is fixed. This means Avionics 1 power up left PFD in reversionary mode for engine start
and Avionics 2 power up MFD and right PFD after engine start. The problem is that now for some reason there's a strange white
backlight in the screens that I can't get rid off without disabling the reversionary mode.

https://user-images.githubusercontent.com/50115960/93968595-58563380-fd40-11ea-9961-c01d2324136a.png (Image of the problem)

To enable the reversionary mode I added the section:

  <Logic> 
	<Handler>Systems_AS1000</Handler>
	<PFD>AS1000_PFD</PFD>
	<MFD>AS1000_MFD</MFD>
  </Logic>

to the panel.xml file.