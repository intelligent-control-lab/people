# Intelligent Control Lab People Directory

This repository contains structured data for managing and displaying information about former lab members in the [Intelligent Control Lab (ICL)](http://icontrol.ri.cmu.edu/) at Carnegie Mellon University.

The data in this repository is used to generate the alumni listing on our lab website:

📄 **Website link**: [http://icontrol.ri.cmu.edu/people/alumni.html](http://icontrol.ri.cmu.edu/people/alumni.html)

---

## 📁 Repository Structure

All member information is stored in a JSON file located at:

```
alumni.json
```

Each entry in this file represents one person. The JSON format is designed to be human-editable and extendable.

---

## 📝 Entry Format

Each person is represented as an object with the following fields:

| Field              | Description                                                                                    |
| ------------------ | ---------------------------------------------------------------------------------------------- |
| `name`             | Full name in the format `"Last, First"`                                                        |
| `image`            | Name of the image file (without extension) in `assets/images/people/` in the private git repo. |
| `email`            | Email address (optional)                                                                       |
| `current_position` | Current job or role (e.g., "Research Scientistic at Amazon Robotics")                          |
| `history`          | A list of program history objects (see below)                                                  |
| `homepage`         | Personal or professional website link (optional)                                               |
| `github`           | GitHub profile link (optional)                                                                 |
| `scholar`          | Google Scholar profile link (optional)                                                         |
| `linkedin`         | LinkedIn profile link (optional)                                                               |
| `x`                | Twitter (X) profile link (optional)                                                            |
| `cv`               | Link to CV (optional)                                                                          |
| `note`             | Additional notes (e.g., co-advisors, special roles)                                            |
| `index`            | Used for sorting display order. Follows these conventions:                                                                               |
|                    | - PhD: simple integer values like `1`, `2`, `3` for order                                                                                |
|                    | - Postdoc: `yyyydd` where `yyyy` is the finishing year and `dd` is an ID with `01`, `02`, `03` for order                                 |
|                    | - Master: `yyyymmdd` where `yyyy` is the year, `mm` is the semester (`01` for Spring, `02` for Summer, `03` for Fall), and `dd` is an ID |

Each `history` object includes:

| Field        | Description                                         |
| ------------ | --------------------------------------------------- |
| `program`    | Degree program (e.g., "PhD", "Master") or other role (e.g., "Intern") |
| `department` | Department affiliation (e.g., "Robotics Institute") |
| `track`      | Optional program track (if applicable)              |
| `start_date` | Start date (e.g., `"Fall 2019"`, optional)          |
| `end_date`   | End date (e.g., `"Spring 2023"`)                    |
| `thesis`     | Thesis title (optional)                             |

---

## ✍️ How to Add or Edit Entries

1. Clone this repository:

   ```bash
   git clone https://github.com/intelligent-control-lab/people.git
   cd people
   ```

2. Open `alumni.json` in your favorite text editor.

3. Add a new JSON object with the appropriate fields, or modify an existing one. Make sure to:

   * Keep commas between entries.
   * Ensure the overall file remains valid JSON.

4. Commit and push your changes:

   ```bash
   git add alumni.json
   git commit -m "Add/update alumni entry for [Name]"
   git push
   ```

---

## 🧩 TODOs

* [ ] **Support remote image specification**
  Currently, the `image` field assumes local files under `assets/images/people/`. We plan to add support for referencing remote images via full URLs (e.g., `https://example.com/avatar.jpg`).
* [ ] **Synchronize thesis information**
  Synchronize the thesis entry with the bib entry in [https://github.com/intelligent-control-lab/Literature](https://github.com/intelligent-control-lab/Literature).

---

## 📬 Questions?

Feel free to open an issue or contact the repo maintainers for assistance.
