# PES VCS Lab Report

## 📌 Overview

This project implements a simplified version control system similar to Git. It includes object storage, tree structures, indexing, and commit history tracking using SHA-based content addressing.

---

## ✅ Phase 1: Object Storage

### Description

In this phase, objects (blobs) are stored using a content-addressable system. Each object is hashed and stored in `.pes/objects`.

### Key Concepts

* SHA-based hashing
* Deduplication (same content → same hash)
* Object format: `"blob <size>\0<data>"`

### Output

* Successfully stored blobs
* Deduplication verified
* Integrity check passed

---

## ✅ Phase 2: Tree Objects

### Description

Tree objects represent directory structures. Each tree stores metadata about files and their corresponding object IDs.

### Key Concepts

* Directory representation
* Linking file names to object IDs
* Recursive structure

---

## ✅ Phase 3: Index (Staging Area)

### Description

The index stores information about staged files before committing.

### Key Concepts

* Tracks file paths
* Stores object IDs
* Acts as staging area before commit

---

## ✅ Phase 4: Commits

### Description

Commits store snapshots of the repository. Each commit points to a tree and optionally a parent commit.

### Key Concepts

* Commit history
* Parent-child relationships
* Reference updates (`HEAD`, `refs/heads/main`)

---

## 🧪 Integration Test

All integration tests passed successfully.

---

## 📸 Screenshots

(Add screenshots here if required)

---

## 🧠 Analysis Questions

### Q5.1: Why use content-addressable storage?

Content-addressable storage ensures that identical data is stored only once. It provides deduplication, integrity verification, and efficient storage.

---

### Q5.2: What is the purpose of hashing?

Hashing uniquely identifies content. It ensures data integrity and allows quick comparisons without reading full data.

---

### Q5.3: Why separate objects and references?

Objects store actual data, while references store pointers to commits. This separation allows efficient version tracking and history management.

---

### Q6.1: How does staging differ from committing?

Staging (index) prepares changes, while committing permanently records them in the repository history.

---

### Q6.2: Why is HEAD important?

HEAD points to the current commit. It helps track the latest state of the repository and enables navigation through history.

---

## ✅ Conclusion

The project successfully demonstrates how a version control system works internally, including object storage, indexing, and commit management.
