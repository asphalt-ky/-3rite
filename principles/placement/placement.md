# Placement
## Placement rules for $T_1$ and $T_2$

This document defines lightweight placement rules for $T_1$ and $T_2$.
The focus is on classification rules for relative placement.

### 1. Basic rules

#### 1.1 Structures must not interfere with each other.
#### 1.2 Placement is classified by whether a $VS$ center of one structure is inside the inner region of the other structure.

### 2. Overlay mode definitions

Let the following predicates be defined:

- $I_{12}$: at least one $VS$ center of $T_1$ is inside the inner region of $T_2$.
- $I_{21}$: at least one $VS$ center of $T_2$ is inside the inner region of $T_1$.

The overlay modes are:

#### 2.1 Mutual inner placement mode
- One $VS$ from $T_1$ and one $VS$ from $T_2$ are each placed in the other structure's inner region.
- Condition: $I_{12}=\mathrm{true}$ and $I_{21}=\mathrm{true}$  
![images not found](./images/placement-mode-1.jpg)  

#### 2.2 $T_1$-to-$T_2$ inner placement mode
- One $VS$ from $T_1$ is placed in the inner region of $T_2$.
- Condition: $I_{12}=\mathrm{true}$ and $I_{21}=\mathrm{false}$  
![images not found](./images/placement-mode-2.jpg)  

#### 2.3 $T_2$-to-$T_1$ inner placement mode
- One $VS$ from $T_2$ is placed in the inner region of $T_1$.
- Condition: $I_{12}=\mathrm{false}$ and $I_{21}=\mathrm{true}$  
![images not found](./images/placement-mode-3.jpg)  

### 3. Notes

#### 3.1 The three overlay modes above are mutually exclusive under the two predicates $I_{12}$ and $I_{21}$.
#### 3.2 A mode remains the same even if multiple $VS$ centers satisfy the same condition.
#### 3.3 Any placement that violates non-interference is invalid regardless of mode.
#### 3.4 Outer-separated placement ($I_{12}=\mathrm{false}$ and $I_{21}=\mathrm{false}$) is geometrically possible, but it is not included in overlay modes because it does not satisfy the basic rule context for overlap classification.


