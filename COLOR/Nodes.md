#Serial vs 
### Parallel node
**1. Independent corrections**
- Node 1: Exposure
- Node 2: Skin tone
- Node 3: Sky adjustment
They don't interfere with each other.

**2. Avoid color contamination**  
Serial:
```
Contrast → Saturation
```
The saturation node sees the already-contrasted image.
Parallel:
```
Contrast        ↘         Parallel Mixer        ↗Saturation
```
Both work from the original image and are merged later.