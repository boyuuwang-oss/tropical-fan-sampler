# Tropical Fan Sampler

An interactive page that runs the tropical samplers of 3D φ³ theory live in the browser. The graphs are the 1PI two-point graphs, and the page follows the paper's three stages:

- **Diagram tropical** integrates one fixed graph. A recursion over all 2^E edge subsets draws a Hepp sector edge by edge, largest first, and the sample is reweighted by w = (U^tr/U)^{3/2} (Σα)^{−ω}. The page shows the exact sector probabilities and checks the result against the exact one- and two-loop values. It stops at L = 7, where the table already has 2^20 entries per graph.
- **Global tropical** draws the graph and its Schwinger parameters together, exactly from the tropical measure on the moduli space of metric graphs. The page draws that space as a tropical fan, with one cone per graph. Step by step, it shows how one sample is made:
  - the largest edge is drawn first;
  - the rest of the graph is cut open into a chain of beads and bridges;
  - each bead with loops is drawn by the same rule, one scale down;
  - the sample is reweighted by w = (U^tr/U)^{3/2} · Π u^δ.
- **Annealed importance sampling** walks the same samples from the tropical measure to the true integrand.

For L = 1–18 the page shows the estimates of the self-energy coefficients s_L against the reference values of the paper, the spread of the log-weights, and each graph's share of s_L. Formulas are typeset with the browser's built-in MathML. The page is in English and Chinese, and works on phones.

It is a single self-contained `index.html`; the only external resources are Google Fonts.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

and go to <http://localhost:8000/>.

## Paper

I. Moult and B. Wang, *Instanton Structure from 325-Loop 3D φ³ Perturbation Theory*, arXiv:XXXX.XXXXX (to be added).

## License

MIT, see [LICENSE](LICENSE).
