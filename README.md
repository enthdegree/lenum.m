# lenum.m
Find the shortest vector of a lattice using exhaustive enumeration.

### Inputs: 
 - `mtx_M` = real matrix, columns define a lattice. Must not have any zero singular values. If it does, either `mtx_M` does not define a discrete lattice or it contains redundant columns.

### Outputs:
 - `v_short` = shortest vector in the lattice.
 - `v_idx` = index of v_short with respect to the basis passed in. In other words, `v_short = mtx_M*v_idx`

Near-verbatim implementation of `ENUM` from the following reference:
    {
      @article{schnorr1994lattice,
      title={Lattice basis reduction: Improved practical algorithms and solving subset sum problems},
      author={Schnorr, Claus-Peter and Euchner, Martin},
      journal={Mathematical programming},
      volume={66},
      number={1-3},
      pages={181--199},
      year={1994},
      publisher={Springer}
    }
