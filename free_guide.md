================================================================================
 THE ULTIMATE SKETCHWARE PRO .SWB ENGINEERING GUIDE
 FREE TIER - FOUNDATION
 Generate a .swb that imports and builds. Zero to working APK.
================================================================================

Target: Sketchware Pro v7.0.0 (versionCode 150)
Revision 5. Verified against the Sketchware Pro 7.0.0 source tree
(BackupFactory, ProjectBuilder, ViewBean, ViewBeans, ComponentBean, BlockBean,
ExtraBlockInfo, ExtraBlockFile, ComponentsHandler, AndroidManifestInjector,
SvgUtils, Material3LibraryManager, BuiltInLibraries, Jx/Lx/Fx/Ox/mq/kq)
AND against real projects that import and build.
Device baseline: Android SDK 31, arm64. Build mode: D8 + Java 1.8.

HOW TO USE THIS DOCUMENT
------------------------
Give it to an AI assistant as reference material, in full, before asking it to
build anything. It is written to be read by a model with no prior Sketchware
knowledge. It is equally readable by a human.

WHAT THIS TIER IS
-----------------
This is the FREE tier. It contains everything needed to generate a .swb that
imports cleanly, opens without crashing, and builds to a working APK with a real
layout. It is complete and honest for what it covers - nothing here is crippled
or withheld mid-explanation.

What it will get you: single-screen and simple multi-screen apps, correct
encryption, correct widget structure, a working Python generator.

What it will NOT get you: logic and event generation, components, Firebase,
resources and SVG injection, Java UI injection, the manifest injection files,
the pre-flight validator, the crash catalog, custom blocks, custom components,
or the build-pipeline internals. Those are the Standard and Premium tiers.

If the free tier produces a working app for you, the paid tiers are the same
document with the other 30 sections restored.

================================================================================
 TABLE OF CONTENTS
================================================================================
 0.  THE GOLDEN RULES (the ones that actually bite)
 1.  WHAT A .SWB IS (ZIP anatomy, restore() flow)
 2.  ENCRYPTION (the #1 crash source)
 3.  THE TWELVE FILES - every format, field by field
 4.  THE LAYOUT SYSTEM - XML <-> drag-and-drop equivalence
 5.  CONTAINER CAPACITY RULES - who holds one child vs. many
 6.  THE COMPLETE WIDGET TYPE-CODE TABLE (all 49 codes, 0-48)
 7.  THE WIDGET JSON SCHEMA - every field explained
 8.  COLORS, SIZES, GRAVITY, ORIENTATION - the numeric encodings
9.  THE PYTHON GENERATOR - architecture + helper functions
10.  RECOMMENDED GENERATION WORKFLOW
11.  QUICK REFERENCE CARD

Section numbers are kept identical across all three tiers, so a number always
means the same thing. Gaps are the sections that live in Standard and Premium.
