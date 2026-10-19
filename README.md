# Tropical Fan Sampler

An interactive page that runs global tropical sampling of φ³ Feynman graphs live in the browser. The graphs are the 1PI two-point graphs of 3D φ³ theory.

Each sample is one cubic graph together with its Schwinger parameters, drawn exactly from the tropical measure on the moduli space. The page draws that space as a tropical fan, with one cone per graph. Step by step, the page shows how one sample is made:

- the largest edge is drawn first;
- the rest of the graph is cut open into a chain of beads and bridges;
- each bead with loops is drawn by the same rule, one scale down;
- the sample is reweighted by w = (U^tr/U)^{3/2} · Π u^δ.

The page also runs annealed importance sampling, which walks the same samples from the tropical measure to the true integrand. For L = 1–18 it shows the estimates of the self-energy coefficients s_L against reference values, the spread of the log-weights, and each graph's share of s_L. The page is in English and Chinese.

It is a single self-contained `index.html`; the only external resources are Google Fonts.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

and go to <http://localhost:8000/>.

## Paper

I. Moult and B. Wang, *Instanton Structure from 325-Loop Perturbation in 3D φ³ Theory*, arXiv:XXXX.XXXXX (to be added).

## License

MIT, see [LICENSE](LICENSE).
