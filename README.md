# ⚛️ Notebooks — Optimización Cuántica en la Práctica

Demos en vivo de Jupyter Notebook para el taller **"Más allá del hype: Realidades y Estrategias Híbridas para la Ventaja Cuántica"** — QPeru, CS Week Perú 2026.

Cada notebook corresponde a una de las 5 pausas prácticas del taller y corre código real de Qiskit, no simulaciones de juguete decorativas — los resultados que ves en cada uno fueron ejecutados y verificados antes de la sesión.

---

## 📂 Contenido

| # | Notebook | Se usa después de... | Qué demuestra |
|---|----------|----------------------|----------------|
| 1 | [`1_por_que_hpc_no_alcanza.ipynb`](./1_por_que_hpc_no_alcanza.ipynb) | Bloque de apertura | Crecimiento exponencial (2ⁿ) vs. tiempo de cómputo clásico — el "muro" combinatorio |
| 2 | [`2_fundamentos_en_codigo.ipynb`](./2_fundamentos_en_codigo.ipynb) | Fundamentos + NISQ | Superposición (Hadamard) y entrelazamiento (estado de Bell), medidos 1000 veces |
| 3 | [`3_qaoa_maxcut_en_vivo.ipynb`](./3_qaoa_maxcut_en_vivo.ipynb) | Cómputo Híbrido (QAOA/VQE/Annealing) | QAOA resolviendo Max-Cut sobre un grafo en vivo, con la audiencia adivinando el corte óptimo |
| 4 | [`4_vqe_molecula_h2.ipynb`](./4_vqe_molecula_h2.ipynb) | 5 industrias, 5 casos | VQE calculando la energía del estado base de H₂, con precisión química real (< 1.6 mHa) |
| 5 | [`5_barren_plateaus_en_vivo.ipynb`](./5_barren_plateaus_en_vivo.ipynb) | Frontera 2025–2026 | Varianza del gradiente cayendo exponencialmente con el número de qubits — el fenómeno de Barren Plateaus, medido en vivo |

---

## 🚀 Cómo correrlos

Cada notebook trae su propia celda de instalación al inicio (`!pip install ...`) con solo las dependencias que necesita. Si estás en un entorno con Python "externally managed" (Debian/Ubuntu recientes) y te sale un error al instalar, agrega la bandera `--break-system-packages`:

```bash
pip install qiskit qiskit-aer --break-system-packages
```

**Requisitos generales del taller:**

```bash
pip install qiskit qiskit-aer qiskit-algorithms qiskit-optimization qiskit-nature pyscf networkx matplotlib numpy
```

**Para correr uno específico:**

```bash
jupyter notebook 3_qaoa_maxcut_en_vivo.ipynb
```

o si prefieres ejecutarlo de punta a punta desde la terminal (útil para probar antes de la sesión en vivo):

```bash
jupyter nbconvert --to notebook --execute --inplace 3_qaoa_maxcut_en_vivo.ipynb
```

---

## 🧠 Stack técnico

- [Qiskit](https://www.ibm.com/quantum/qiskit) 2.x — circuitos y algoritmos cuánticos
- [Qiskit Nature](https://qiskit-community.github.io/qiskit-nature/) + [PySCF](https://pyscf.org/) — química cuántica (VQE)
- [Qiskit Optimization](https://qiskit-community.github.io/qiskit-optimization/) — formulación QUBO/Max-Cut (QAOA)
- NumPy / Matplotlib / NetworkX — cómputo numérico y visualización

---

## 📜 Licencia y créditos

Material educativo desarrollado por **QPeru**, capítulo aspirante de QWorld en Perú, para uso libre en talleres, charlas y actividades de divulgación de la comunidad.

<div align="center">

🇵🇪 **QPeru** · Chapter aspirante de QWorld

</div>
