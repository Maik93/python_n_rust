# Python and Rust together
Everything here is extracted from https://www.maturin.rs.

## How to make a new project
A new project can be created in two different ways (choose only one!):
- `cargo new --lib --edition 2021 rust_n_python` and then edit `Cargo.toml` and `pyproject.toml` as in this repo;
- `maturin new -b pyo3 rust_n_python` and add the `abi3-py37` feature to `Cargo.toml`, as in this repo.

Set maturin in a venv (suggested, as it will automatically install the module there):
```bash
python -m venv venv
source venv/bin/activate
pip install -U pip maturin
```

## Build the python module
Maturin can build and install the module inside your venv with `maturin develop`.
Once you get something that can be released, use `maturing build` instead to generate a wheel file.
