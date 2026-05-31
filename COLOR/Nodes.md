# Serial vs Parallel
- **Serial nodes** = applying filters one after another.
- **Parallel nodes** = several editors each get the original photo, make their own changes, then the results are combined.
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
### Serial Nodes
simply one node after other and one transform after other , each node Works on the output of the previous node.

## Layer nodes
**Layer Mixer** is different from a **Parallel Mixer**.

### Parallel Mixer

```
Input → Node A →                  → Parallel Mixer → OutputInput → Node B →
```

Both nodes get the same image, and Resolve combines their corrections mathematically.

---
### Layer Mixer

```
Background →              → Layer Mixer → OutputForeground →
```

It works more like **Photoshop layers**.

The node connected to the **green input** is on top.  
The node below it is underneath.

You can use blend modes such as:

- Add
- Multiply
- Screen
- Overlay
- Soft Light

just like Photoshop.