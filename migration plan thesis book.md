# Migration plan: Thesis Book to Prism

## Goal

Import the first three chapters and approximately 30 sources into the current LaTeX project. Preserve citation keys, existing work and the destination template. Keep Zotero as the main reference manager.

## Steps

1. **Upload the old project:** Preferably a ZIP containing `.tex`, original `.bib`, figures and custom definitions. Use the original bibliography to preserve existing citation keys.
2. **Inspect and map:** Match content to destination sections. Check missing citations, conflicting keys, duplicate labels, file paths and template dependencies.
3. **Pilot one section:** Show proposed changes, obtain approval, migrate and compile with BibLaTeX/Biber. Check citations, references and layout.
4. **Migrate remaining content:** Apply approved changes in batches, preserve unrelated work and compile again.
5. **Add PDFs:** Upload Zotero attachments and map each PDF to its citation key and document version using relative paths. Local Windows paths are not accessible in Prism.
6. **Test evidence checking:** Compare a cited paragraph with its paper. Report supporting pages, qualifications and unsupported claims separately from issues in the thesis's argument.

## Safeguards and updates

- No thesis or bibliography changes without explicit approval.
- Preserve citation keys; matching a title or DOI alone does not preserve LaTeX citations.
- Maintain metadata in Zotero. Review updated exports before merging into `references.bib`; no automatic synchronization or overwriting.

## Next action

Upload the old project for inspection and a concrete merge proposal.