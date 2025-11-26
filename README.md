# SASOK Emotional Recognition Platform - macOS Native App

![Platform](https://img.shields.io/badge/platform-macOS%2015.0+-blue)
![Swift](https://img.shields.io/badge/Swift-6.0-orange)
![License](https://img.shields.io/badge/license-Proprietary-red)
![Status](https://img.shields.io/badge/status-Development-yellow)

## Overview

SASOK Emotional Recognition Platform is a **privacy-first**, **on-device** emotional intelligence system for macOS. Built with **SwiftUI** and **CoreML**, it provides real-time multimodal emotion analysis through facial expressions, voice patterns, and eye movement tracking.

### Key Features

- ✅ **Multimodal Emotion Fusion** - Combines facial, voice, and physiological signals
- ✅ **100% On-Device Processing** - Zero cloud dependency, all inference via CoreML
- ✅ **AES-256-GCM Encryption** - Military-grade local data protection
- ✅ **Conflict Detection** - Identifies disagreements between emotional modalities
- ✅ **Temporal Analysis** - Track emotional patterns over time (Persona Timeline)
- ✅ **Liveness Detection** - Anti-spoofing protection against photo/video attacks
- ✅ **GDPR/HIPAA Ready** - Privacy-by-design architecture

## Architecture

```
SASOK-Emotional-macOS/
├── SASOKEmotional/
│   ├── App/
│   │   ├── SASOKEmotionalApp.swift        # App entry point
│   │   └── ContentView.swift              # Main UI container
│   ├── Models/
│   │   ├── EmotionState.swift             # Emotion data models
│   │   ├── BiometricData.swift            # Facial/voice/eye data
│   │   └── PersonaProfile.swift           # User emotional profile
│   ├── ViewModels/
│   │   ├── EmotionRecognitionViewModel.swift
│   │   └── PersonaViewModel.swift
│   ├── Views/
│   │   ├── CameraView.swift
│   │   ├── AudioVisualizerView.swift
│   │   ├── EmotionDashboardView.swift
│   │   ├── PersonaTimelineView.swift
│   │   └── PrivacySettingsView.swift
│   ├── Services/
│   │   ├── CameraService.swift            # AVFoundation camera
│   │   ├── AudioService.swift             # Audio capture
│   │   ├── FaceAnalysisService.swift      # Vision framework
│   │   ├── VoiceAnalysisService.swift     # Audio emotion analysis
│   │   ├── MLModelService.swift           # CoreML inference
│   │   ├── LocalStorageService.swift      # Encrypted persistence
│   │   ├── LivenessDetectionService.swift # Anti-spoofing
│   │   └── SASOKEthicsService.swift       # Privacy controls
│   ├── MLModels/
│   │   ├── EmotionClassifier.mlmodel      # Facial emotion model
│   │   └── VoiceEmotionModel.mlmodel      # Audio emotion model
│   └── Resources/
│       ├── Info.plist
│       └── Assets.xcassets
└── Tests/
    └── SASOKEmotionalTests/
```

## Requirements

- **macOS**: 15.0+ (Sequoia/Tahoe)
- **Xcode**: 16.0+
- **Swift**: 6.0
- **Hardware**: Camera + Microphone (built-in or external)

## Installation

### 1. Clone Repository

```bash
git clone https://github.com/TSheylock/SASOK-Emotional-macOS.git
cd SASOK-Emotional-macOS
```

### 2. Open in Xcode

```bash
open SASOKEmotional.xcodeproj
```

### 3. Configure Signing

- Select project in Xcode navigator
- Go to **Signing & Capabilities**
- Select your development team
- Xcode will auto-generate provisioning profile

### 4. Add CoreML Models

**Currently the project uses placeholder models. To enable full functionality:**

1. Train or download emotion classification models:
   - Facial: FER2013 or AffectNet dataset
   - Voice: RAVDESS or CREMA-D dataset

2. Place `.mlmodel` files in `SASOKEmotional/MLModels/`

3. Rebuild project (⌘B)

### 5. Grant Permissions

On first run, macOS will prompt for:
- **Camera** access (for facial analysis)
- **Microphone** access (for voice emotion detection)

These are required for core functionality.

## Privacy Controls

Access via **SASOK Emotional → Settings...** (⌘,)

- **Consent Level**: Full / Limited / Anonymized / None
- **Data Retention**: Permanent / 30 Days / 7 Days / Session Only
- **Emotional Boundaries**: Exclude specific emotions from recording
- **Autonomy Level**: 1-10 scale (SASOK framework)

## SASOK Integration

This app integrates with the broader **SASOK** (Self-Augmented Symbiotic Organism Kernel) ecosystem:

- **XoReflect**: Emotional Signature Archive for long-term memory
- **XoEthics**: Autonomy level enforcement and ethical boundaries
- **XoConsent**: Granular user consent management
- **XoShield**: Cognitive firewall for data protection

## Roadmap

### Phase 1: MVP (Weeks 1-4) ✅
- [x] Project structure
- [x] Camera/audio capture
- [x] Basic UI with SwiftUI
- [x] Local storage with encryption

### Phase 2: CoreML Integration (Weeks 5-8)
- [ ] Train facial emotion model (FER2013)
- [ ] Train voice emotion model (RAVDESS)
- [ ] Export to CoreML format
- [ ] Integrate with MLModelService

### Phase 3: Advanced Features (Weeks 9-12)
- [ ] Liveness detection implementation
- [ ] Temporal emotion prediction (LSTM)
- [ ] ARKit eye tracking integration
- [ ] PDF report generation

### Phase 4: Production (Weeks 13-16)
- [ ] App Store submission
- [ ] Notarization
- [ ] Privacy Nutrition Label
- [ ] User documentation

## License

**Proprietary License** - © 2025 Teymur Safiulov / Evorin LLC

All rights reserved. Unauthorized copying, modification, or distribution is prohibited.

For licensing inquiries: teymur@evorin.com

## Contact

- **Author**: Teymur Safiulov
- **Company**: Evorin LLC
- **Email**: teymur@evorin.com
- **Website**: [saske.xyz](https://saske.xyz)
- **LinkedIn**: [TSheylock](https://linkedin.com/in/tsheylock)

---

**Built with ❤️ for symbiotic human-AI interaction**
