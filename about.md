---
title: "About This Project"
---

### Motivation  
Deep policies often fail in cluttered or novel scenes, risking hardware damage.

### Methodology  
1. **Safe-Set Extraction**  
   - Sample poses around demonstrations  
   - Filter by continuous FOV score  
   - Filter by Mahalanobis recognizability

2. **Safety Function**  
   \[
     h(x)=\mathrm{FOV}(x)\times\exp\bigl(-d_M(x)^2\bigr)
   \]

3. **Runtime Recovery**  
   \[
     u^*=\arg\min_{u}\|u-u_\pi\|^2\quad\text{s.t.}\;\nabla h(x)^\top u\ge -\alpha\,h(x).
   \]

### Results  
![Results Table](/assets/results_table.png){: .center}  
- Sim Clean: 0.95→1.00, Clutter: 0.50→0.85  
- Real Clean: 0.62→0.88, Clutter: 0.55→0.80

### Future Work  
- Dynamic goals, learned control barriers  
- Grasp‐feasibility integration  
