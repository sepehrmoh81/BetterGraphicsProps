# BetterGraphicsProps
Magisk Module For Better Graphics/Reducing Lag on AOSP-Based ROMs and GSIs.
## Issue
The issue mentioned here: https://github.com/phhusson/treble_experimentations/issues/230

> Animations get very laggy almost like dropped frames while opening or switching apps.

The issue is persistent between different devices. This module fixes laggy animations/stutters by changing these props:

> debug.sf.hw=0  
debug.egl.hw=0  
debug.enable.sglscale=1  
debug.sf.enable_hwc_vds=1  
debug.gralloc.enable_fb_ubwc=1  
debug.sf.latch_unsignaled=1  
debug.sf.recomputecrop=0  
dev.pm.dyn_samplingrate=1

## Notes
1. This module **won't help you with your slow phone!** Although this might help you with your daily experience, if your phone feels laggy all the time consider changing CPU/GPU clocks at the cost of battery usage. The props are for situations where there are slight stutters in an overall smooth experience.
2. Pixel phones probably won't need any of these props