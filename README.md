# Bachelor of Engineering (B.E) - Mumbai University Notes & Textbooks

<p align="center">
  <b>The Ultimate Open-Source Repository for Mumbai University Engineering Students</b><br>
  <i>Get access to comprehensive study materials, semester notes, textbooks, and resources for all branches under Mumbai University (MU).</i>
</p>

## 🔍 About This Repository (Search Keywords & Topics)

Welcome to the **Bachelor of Engineering - Mumbai University Notes** repository! This project serves as a centralized hub to find all the essential academic resources needed by engineering students affiliated with **Mumbai University (MU)**. 

Whether you are looking for **first-year engineering notes**, **core subject textbooks**, or **department-specific study materials**, you will find it neatly organized here. 

**Targeted Keywords for Searchability:** `Mumbai University Engineering Notes`, `MU B.E Notes`, `MU B.Tech Notes`, `Mumbai University Textbooks PDF`, `Semester 1 to Semester 8 Notes`, `AIML Notes`, `Computer Engineering Notes MU`, `IT Notes MU`, `Mechanical Engineering Materials`, `Civil Engineering Textbooks MU`, `Electrical Engineering Books`, `Automobile Engineering Notes`.

---

## 🏛 Supported Departments & Branches

We cover study materials for the following major engineering departments at Mumbai University:
- 💻 **Computer Engineering** (COMP)
- 🌐 **Information Technology** (IT)
- 🤖 **Artificial Intelligence and Machine Learning** (AIML)
- ⚙️ **Mechanical Engineering** (MECH)
- 🏗️ **Civil Engineering** (CIVIL)
- ⚡ **Electrical Engineering** (ELEC)
- 🚗 **Automobile Engineering** (AUTO)

---

## 📂 Repository Folder Structure (Semester-wise)

To ensure that you can find the exact file quickly, the repository is organized chronologically by **Academic Year**, **Engineering Department**, **Semester**, and **Resource Type** (Textbooks or Notes). 

```text
Bachelor_of_Engineering_Mumbai_University_Notes/
├── first_year/
│   ├── sem_1/ (NOTES / TEXTBOOKS)
│   └── sem_2/ (NOTES / TEXTBOOKS)
├── second_year/
│   ├── AIML, AUTOMOBILE, CIVIL, COMPUTER, ELECTRICAL, IT, MECHANICAL/
│       ├── sem_3/ (NOTES / TEXTBOOKS)
│       └── sem_4/ (NOTES / TEXTBOOKS)
├── third_year/
│   ├── AIML, AUTOMOBILE, CIVIL, COMPUTER, ELECTRICAL, IT, MECHANICAL/
│       ├── sem_5/ (NOTES / TEXTBOOKS)
│       └── sem_6/ (NOTES / TEXTBOOKS)
└── fourth_year/
    ├── AIML, AUTOMOBILE, CIVIL, COMPUTER, ELECTRICAL, IT, MECHANICAL/
        ├── sem_7/ (NOTES / TEXTBOOKS)
        └── sem_8/ (NOTES / TEXTBOOKS)
```

---

## 🤝 Open to Contribute (Join the Community!)

This repository thrives on contributions from students, teachers, and alumni! If you have **Mumbai University question papers, handwritten notes, PPTs, or PDF textbooks**, please contribute to help thousands of future engineers.

### 📜 Strict Contribution Rules (For SEO and Organization)

To maintain consistency and make it easy for search engines and students to find files, please strictly adhere to the following rules when contributing:

1. **Use Full Forms for File Names (Crucial for Search Results):**
   - **DO NOT** use abbreviations or acronyms for file names. Search tools look for full subject names.
   - ❌ **Wrong:** `RL.pdf` (Hard to find)
   - ✅ **Correct:** `Reinforcement_Learning.pdf` (Highly searchable)
   - ❌ **Wrong:** `DBMS.pdf`
   - ✅ **Correct:** `Database_Management_Systems.pdf`

2. **No Spaces in File Names:**
   - File names must not contain any spaces. Use underscores (`_`) instead of spaces to avoid broken links.
   - ❌ **Wrong:** `Machine Learning Notes.pdf`
   - ✅ **Correct:** `Machine_Learning_Notes.pdf`

3. **Correct Placement in the Hierarchy:**
   - Ensure you are uploading the document in the correct year, department, semester, and respective `TEXTBOOKS` or `NOTES` folder. 

4. **Use Git CLI for Uploads:**
   - Because textbooks and notes can be large, **do not upload files manually via the GitHub web interface**. Always use the Git Command Line Interface (CLI) to push your files.
   - See the full **Git LFS guide** below for step-by-step instructions.

5. **Standardized Commit Message Format:**
   - When making a commit, clearly state what was added, where it was added, and avoid vague messages.
   - **Format:** `Added : [File_Name] in SEM [Number], [Year]`
   - ✅ **Example:** `Added : Reinforcement_Learning_Textbook in SEM 8, Fourth_year`

Thank you for contributing and making the **Mumbai University Engineering** community stronger!

---

## 📦 Uploading Large Files with Git LFS (Large File Storage)

GitHub has a **strict 100 MB file size limit**. Most textbooks and reference PDFs easily exceed this. This is why this repository uses **Git LFS (Large File Storage)** — a Git extension that stores large files separately while keeping your repository fast and lightweight.

> **Git LFS replaces large files with lightweight text pointers inside Git, while storing the actual file content on a remote server.**

---

### ⚙️ Step 1 — Install Git LFS

Download and install Git LFS from the official website:
👉 [https://git-lfs.github.com](https://git-lfs.github.com)

After installation, run this **once** on your machine to initialize it:

```bash
git lfs install
```

---

### 📥 Step 2 — Clone the Repository

```bash
git clone https://github.com/theyashva/Bachelor_of_Engineering_Mumbai_University_Notes.git
cd Bachelor_of_Engineering_Mumbai_University_Notes
```

> Git LFS will automatically pull the actual file content when you clone, since `.gitattributes` is already configured to track `*.pdf` files.

---

### 📁 Step 3 — Place Your File in the Correct Folder

Navigate to the correct folder before adding your file. Example:

```
fourth_year/AIML/sem_8/TEXTBOOKS/
```

Make sure:
- The file name uses **Full Form** (no abbreviations)
- The file name uses **underscores** instead of spaces
- ✅ Example: `Reinforcement_Learning.pdf`

---

### ➕ Step 4 — Stage, Commit & Push

```bash
# Stage the new file
git add fourth_year/AIML/sem_8/TEXTBOOKS/Reinforcement_Learning.pdf

# Commit with the standard format
git commit -m "Added : Reinforcement_Learning in SEM 8, Fourth_year"

# Push to the main branch
git push origin main
```

Git LFS will automatically detect and upload the large file via LFS — **no extra steps needed!**

---

### ✅ How to Verify a File is Tracked by LFS

To confirm your file is being stored via LFS (and not as a raw binary), run:

```bash
git lfs ls-files
```

You should see your file listed. If not, ensure the `.gitattributes` file contains:

```
*.pdf filter=lfs diff=lfs merge=lfs -text
```

---

### ⚠️ Common Mistakes to Avoid

| Mistake | Fix |
|---|---|
| Uploading files via GitHub website | Always use Git CLI |
| Pushing without Git LFS installed | Run `git lfs install` first |
| File size over 100 MB pushed without LFS | Migrate using `git lfs migrate import --include="*.pdf"` |
| Spaces in file names | Use underscores: `My_Notes.pdf` |
| Short/abbreviated file names | Use full names: `Database_Management_Systems.pdf` |
