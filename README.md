# PROJECT-NAND2TETRIS-PART-1
PROJECT -01
# nand2tetris — Project 01 (Basic Logic Gates)

**Author:** ARAVINDKUMAR GS
**Course:** From Nand to Tetris / Coursera  
**Date:** 2025-12-03

## Project summary
This repository contains my solutions for **Project 1: Basic Logic Gates** from the Nand2Tetris curriculum. The goal of Project 1 is to implement the elementary logic gates (using only the built-in `Nand` chip) and their 16-bit/aggregated versions. These gates are the building blocks for later projects in the course. :contentReference[oaicite:1]{index=1}

---

## Files included
The repository includes the following `.hdl` files for Project 1:

- `And.hdl`
- `Or.hdl`
- `Not.hdl`
- `Xor.hdl`
- `Mux.hdl`
- `DMux.hdl`
- `And16.hdl`
- `Or16.hdl`
- `Not16.hdl`
- `Or8Way.hdl`
- `Mux16.hdl`
- `DMux4Way.hdl`
- `DMux8Way.hdl`
- `Mux4Way16.hdl`
- `Mux8Way16.hdl`

> Each file implements a single chip. The files were written to match the expected project API (chip name, IN/OUT port declarations and `PARTS:` section).

---

## Example: HDL structure
Below is an example `And.hdl` implementation structure (use this style for other chips):

```hdl
CHIP And {
    IN a, b;
    OUT out;

    PARTS:
    Nand(a=a, b=b, out=n);
    Not(in=n, out=out);
}

Nice — here’s a ready-to-use **`README.md`** you can drop into your GitHub repo for your nand2tetris Project 1 (and other projects). It includes: project description, expected files, how to run the HDL tests, example HDL snippet, and exact `git` commands to push to GitHub.

I looked up the nand2tetris Project 1 description and README templates to make this fit the course style. ([Nand2Tetris][1])

# README.md (copy & paste)

````markdown
# nand2tetris — Project 01 (Basic Logic Gates)

**Author:** Ak  
**Course:** From Nand to Tetris / Coursera  
**Date:** YYYY-MM-DD

## Project summary
This repository contains my solutions for **Project 1: Basic Logic Gates** from the Nand2Tetris curriculum. The goal of Project 1 is to implement the elementary logic gates (using only the built-in `Nand` chip) and their 16-bit/aggregated versions. These gates are the building blocks for later projects in the course. :contentReference[oaicite:1]{index=1}

---

## Files included
The repository includes the following `.hdl` files for Project 1:

- `And.hdl`
- `Or.hdl`
- `Not.hdl`
- `Xor.hdl`
- `Mux.hdl`
- `DMux.hdl`
- `And16.hdl`
- `Or16.hdl`
- `Not16.hdl`
- `Or8Way.hdl`
- `Mux16.hdl`
- `DMux4Way.hdl`
- `DMux8Way.hdl`
- `Mux4Way16.hdl`
- `Mux8Way16.hdl`

> Each file implements a single chip. The files were written to match the expected project API (chip name, IN/OUT port declarations and `PARTS:` section).

---

## Example: HDL structure
Below is an example `And.hdl` implementation structure (use this style for other chips):

```hdl
CHIP And {
    IN a, b;
    OUT out;

    PARTS:
    Nand(a=a, b=b, out=n);
    Not(in=n, out=out);
}
````

> Note: Course graders expect files in the root of the submitted ZIP (not nested in subfolders).

---

## How to run & test locally

1. Download and install the **Hardware Simulator** from the official nand2tetris tools (or use the course-provided software).
2. Open the Hardware Simulator and load the test script or `.tst` for each chip (the course provides `.tst` files).
3. Run the test and inspect the `.cmp` output to verify correctness.

If you want to test quickly from a UNIX shell, you can create the ZIP (which Coursera accepts) with:

```bash
# in the folder that contains your 15 .hdl files:
zip project1.zip *.hdl
```

When you submit to Coursera, make sure the ZIP contains only the `.hdl` files at the root — **no parent folder** inside the ZIP.

---

## GitHub — add & push (quick commands)

If your repo is not set up, run:

```bash
# inside your local project folder
git init
git add .
git commit -m "Project1: Add HDL gates"
# replace the URL below with your GitHub repository's URL
git remote add origin https://github.com/your-username/your-repo.git
git branch -M main
git push -u origin main
```

If repo already exists and you made changes:

```bash
git add .
git commit -m "Update Project1 HDL"
git push
```

---

## Tips & common submission mistakes

* **Do not** include files inside a nested folder in the ZIP; grader expects files at the root.
* File names must **exactly match** the expected names (case-sensitive on some systems).
* Ensure each `.hdl` file contains valid HDL syntax and `PARTS:` definitions.
* If grader reports `file_missing_<Name>`, it usually means wrong ZIP structure or missing files.

  
## References & templates

* Project description and requirements: Nand2Tetris Project 1. ([Nand2Tetris][1])
* README template inspiration: Best README templates on GitHub. ([GitHub][2])


## License

This repository is released under the MIT License. See `LICENSE` for details.

