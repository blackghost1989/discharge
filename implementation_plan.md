# General Surgery Discharge Template Implementation Plan

Adding a second discharge template specialized for general surgeries (Neutering, Tumor removal, etc.) using the same localized UI and persistent library logic.

## Proposed Changes

### [HTML/JS] general_surgery_template.html

- **[NEW] [general_surgery_template.html](file:///Users/stella/.gemini/antigravity/brain/e61de65b-66e6-43c6-a03d-857eef62b929/general_surgery_template.html)**
    - Adapt the dental template's core structure (Two-pane layout, Traditional Chinese).
    - **Shared Library Logic**: Reuse `DENTAL_OPTIONS_LIBRARY` for Veterinary Name, Hospital Info, and Emergency Info to allow cross-template consistency.
    - **New Fields**:
        - Surgery Name / Procedure (Persistent Library).
        - Wound Care Instructions (Persistent Library).
        - Suture Removal / Checkup schedule.
        - Collar (E-collar) instructions.
    - **Specific Logic**:
        - Dynamic rows for Medications.
        - Automatic preview generation.
        - Print-optimized CSS.

## Verification Plan

### Automated Tests (Browser Subagent)
- Verify that common fields like "Vet Name" filled in the Dental template (if saved to library) appear in the General Surgery template's dropdown.
- Test saving new general surgery specific options (e.g., "絕育手術 (Neutering)").
- Test dynamic row addition for medications.
- Verify print preview layout.
