# Independent check of "Same Orbit Implies Same Response" (2026-09-24)

Exact diagonalization written without the paper's code: full 2^N Hilbert space, degenerate ground
states averaged (tolerance 1e-8), all connected graphs with N=6 (112) and N=7 (853).

- `edrn_orbit_response_independent_check.py`: checks A (N=7 orbit/response table), B/C (Hellmann-Feynman
  and how p_S passes 1/2), D (the sector formula (1 - 3<sz sz>)/4 against the true p_S, by total spin),
  H (Hellmann-Feynman on degenerate ground states). Run: `python edrn_orbit_response_independent_check.py --workers 12`
- `edrn_window_boundary_check.py`: where |sd_1(s)| = |sd_2(s)| stops holding in graphs 38, 60, 103 (N=6).
- `edrn_orbit_paper_claims.py`: recomputes every figure in the reply from the result files and from
  the v12/v16 files in the paper's repository.
- `*.result.json`: the outputs these runs produced.
- `seal-4e85d5f8ec30.svg`: the seal on the reply. Transparency log entry 2, root
  5e2ddfbb455fcf76e0e40f9f051931f8c9fca8e8d4407b76352c4e85d5f8ec30,
  proof https://dancenitra.github.io/inspeximus-log/entries/2.proof.json
