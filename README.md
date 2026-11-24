# Mermaid frame test

Each chart uses `layout: dagre`.

## 1. TB chain, 3 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
```

End of chart 1.

## 2. TB chain, 5 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
  s3[Step 3] --> s4[Step 4]
  s4[Step 4] --> s5[Step 5]
```

End of chart 2.

## 3. TB chain, 8 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
  s3[Step 3] --> s4[Step 4]
  s4[Step 4] --> s5[Step 5]
  s5[Step 5] --> s6[Step 6]
  s6[Step 6] --> s7[Step 7]
  s7[Step 7] --> s8[Step 8]
```

End of chart 3.

## 4. TB chain, 12 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
  s3[Step 3] --> s4[Step 4]
  s4[Step 4] --> s5[Step 5]
  s5[Step 5] --> s6[Step 6]
  s6[Step 6] --> s7[Step 7]
  s7[Step 7] --> s8[Step 8]
  s8[Step 8] --> s9[Step 9]
  s9[Step 9] --> s10[Step 10]
  s10[Step 10] --> s11[Step 11]
  s11[Step 11] --> s12[Step 12]
```

End of chart 4.

## 5. TB chain, 20 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
  s3[Step 3] --> s4[Step 4]
  s4[Step 4] --> s5[Step 5]
  s5[Step 5] --> s6[Step 6]
  s6[Step 6] --> s7[Step 7]
  s7[Step 7] --> s8[Step 8]
  s8[Step 8] --> s9[Step 9]
  s9[Step 9] --> s10[Step 10]
  s10[Step 10] --> s11[Step 11]
  s11[Step 11] --> s12[Step 12]
  s12[Step 12] --> s13[Step 13]
  s13[Step 13] --> s14[Step 14]
  s14[Step 14] --> s15[Step 15]
  s15[Step 15] --> s16[Step 16]
  s16[Step 16] --> s17[Step 17]
  s17[Step 17] --> s18[Step 18]
  s18[Step 18] --> s19[Step 19]
  s19[Step 19] --> s20[Step 20]
```

End of chart 5.

## 6. LR chain, 3 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
```

End of chart 6.

## 7. LR chain, 5 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
  s3[Step 3] --> s4[Step 4]
  s4[Step 4] --> s5[Step 5]
```

End of chart 7.

## 8. LR chain, 8 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
  s3[Step 3] --> s4[Step 4]
  s4[Step 4] --> s5[Step 5]
  s5[Step 5] --> s6[Step 6]
  s6[Step 6] --> s7[Step 7]
  s7[Step 7] --> s8[Step 8]
```

End of chart 8.

## 9. LR chain, 12 nodes

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  s1[Step 1] --> s2[Step 2]
  s2[Step 2] --> s3[Step 3]
  s3[Step 3] --> s4[Step 4]
  s4[Step 4] --> s5[Step 5]
  s5[Step 5] --> s6[Step 6]
  s6[Step 6] --> s7[Step 7]
  s7[Step 7] --> s8[Step 8]
  s8[Step 8] --> s9[Step 9]
  s9[Step 9] --> s10[Step 10]
  s10[Step 10] --> s11[Step 11]
  s11[Step 11] --> s12[Step 12]
```

End of chart 9.

## 10. LR chain, 6 nodes, long labels

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  s1[Collect requirements] --> s2[Draft the proposal]
  s2[Draft the proposal] --> s3[Review with the team]
  s3[Review with the team] --> s4[Revise and agree]
  s4[Revise and agree] --> s5[Build the first cut]
  s5[Build the first cut] --> s6[Ship to production]
```

End of chart 10.

## 11. TB chain, 6 nodes, long labels

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  s1[Collect requirements] --> s2[Draft the proposal]
  s2[Draft the proposal] --> s3[Review with the team]
  s3[Review with the team] --> s4[Revise and agree]
  s4[Revise and agree] --> s5[Build the first cut]
  s5[Build the first cut] --> s6[Ship to production]
```

End of chart 11.

## 12. TB tree, 4 children x 2 leaves

```mermaid
---
config:
  layout: dagre
---
flowchart TB
  root[Root]
  root --> c1[Child 1]
  c1 --> g11[Leaf 1.1]
  c1 --> g12[Leaf 1.2]
  root --> c2[Child 2]
  c2 --> g21[Leaf 2.1]
  c2 --> g22[Leaf 2.2]
  root --> c3[Child 3]
  c3 --> g31[Leaf 3.1]
  c3 --> g32[Leaf 3.2]
  root --> c4[Child 4]
  c4 --> g41[Leaf 4.1]
  c4 --> g42[Leaf 4.2]
```

End of chart 12.

## 13. LR tree, 4 children x 2 leaves

```mermaid
---
config:
  layout: dagre
---
flowchart LR
  root[Root]
  root --> c1[Child 1]
  c1 --> g11[Leaf 1.1]
  c1 --> g12[Leaf 1.2]
  root --> c2[Child 2]
  c2 --> g21[Leaf 2.1]
  c2 --> g22[Leaf 2.2]
  root --> c3[Child 3]
  c3 --> g31[Leaf 3.1]
  c3 --> g32[Leaf 3.2]
  root --> c4[Child 4]
  c4 --> g41[Leaf 4.1]
  c4 --> g42[Leaf 4.2]
```

End of chart 13.
