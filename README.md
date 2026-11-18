# Sorting complexity: insertion sort vs merge sort

A small experiment that counts how many basic operations insertion sort and merge sort perform on random arrays of growing size, then plots the two curves.

Version française plus bas.

![Complexity comparison](complexity.png)

## What's inside

| File | Content |
|---|---|
| `complexity_sort.py` | Both algorithms with an instruction counter, run on arrays of 5 to 1000 elements, plot saved as `complexity.png` |
| `Comparaison_tri_matplotlib.ipynb` | The same experiment as a notebook, step by step |
| `Complexity_R.ipynb` | A second notebook used to prepare the R version of the comparison |

## What the plot shows

Insertion sort grows roughly like n², so its curve shoots up as the array gets bigger. Merge sort grows like n log n and stays much flatter. On small arrays the difference is small, which is why some libraries switch to insertion sort for short sub-arrays.

## Run it

```bash
pip install matplotlib
python complexity_sort.py
```

Arrays are random, so the exact numbers change on each run, but the shape of the curves stays the same.

Related repository: [Complexity_with_R](https://github.com/oberlinkeyanfe-ops/Complexity_with_R), where the same comparison is measured in R with the `atime` package.

---

## Version française

Petite expérience qui compte le nombre d'opérations élémentaires du tri par insertion et du tri fusion sur des tableaux aléatoires de taille croissante, puis trace les deux courbes.

Le tri par insertion évolue en n², le tri fusion en n log n. Sur de petits tableaux, l'écart est faible ; sur de grands tableaux, le tri fusion est nettement plus efficace.

Pour lancer : `pip install matplotlib` puis `python complexity_sort.py`.
