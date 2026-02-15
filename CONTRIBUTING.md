# Contributing to GeoLocate 📍

Thank you for contributing! To keep our codebase stable and our geospatial queries efficient, please follow these guidelines.

---

## 🛠 Getting Started

### Clone the Repo
Ensure you have the latest code from the `main` branch.

### Setup Environment

```bash
python -m venv venv
source venv/bin/activate  # venv\Scripts\activate on Windows
pip install -r requirements.txt
```

### Local Database
Connect your local Flask instance to your MongoDB Atlas cluster using your `.env` file.

---

## 🌿 Branching Strategy

We use a structured branching model. **Never commit directly to `main`.**

- **main**  
  The "production" branch. Only contains stable, tested code.

- **feature/**  
  For all new development  
  Example: `feature/spatial-indexing`, `feature/ui-map`

- **bugfix/**  
  For fixing errors found in the code  
  Example: `bugfix/connection-leak`

- **docs/**  
  Specifically for updating READMEs, project documentation, or PPT content.

---

## 📝 Commit Standards

Keep messages short and use the following prefixes:

- `feat:` — New feature
- `fix:` — Bug fix
- `docs:` — Documentation change
- `refactor:` — Code improvement without new features

---

## 🚀 The PR & Review Process

### Branch
Create your branch from main:

```bash
git checkout -b feature/your-feature-name
```

### Sync
Before pushing, pull the latest changes from `main` to avoid conflicts.

### PR Template
Fill out the Pull Request template.

### Peer Review
At least one team member must review and approve your PR before it is merged.

### Test
Ensure your MongoDB `2dsphere` queries work and return results in GeoJSON format.

---

## 💻 Technical Standards

- **Data Format:**  
  All location data must be stored as GeoJSON:

```
[longitude, latitude]
```

- **Indexing:**  
  Any new collection involving locations must have a `2dsphere` index applied.

- **Style:**  
  Follow PEP 8 for all Python/Flask code.
