# Call Flow Builder

A powerful, visual workflow builder designed for creating complex telephony logic for FreeSWITCH-based engines. This tool allows developers and non-technical users to design, visualize, and configure call flows using a drag-and-drop interface.

[Flow Builder Preview](https://flow-builder-ivory.vercel.app/) 

## 🚀 Features

- **Visual Drag-and-Drop Editor**: Built with React, offering an intuitive canvas for designing logic.
- **FreeSWITCH Integration**: Native support for core telephony commands:
  - `call.originate`: Initiate outbound calls.
  - `call.playback`: Play audio files.
  - `call.start_audio_fork`: Stream audio for AI/Transcription.
  - `call.start_recording` / `stop_recording`.
  - `call.amd.start`: Answering Machine Detection.
  - `call.webhook`: External API integrations.
  - And many more (`wait`, `hold`, `transfer`, `displace_audio`).
- **Logic & Transitions**: Visually map call states and events (e.g., `call.channel.answered`, `call.playback.stopped`).
- **Validation**: Real-time validation ensures workflow integrity before exporting.
- **JSON Export**: Generates compliant JSON configurations ready for your FreeSWITCH execution engine.
- **Dark/Light Mode**: Fully themable UI for comfortable usage in any environment.

## 📖 Usage Guide

1.  **Creating Nodes**: Drag items from the **Sidebar** onto the canvas to create new steps (e.g., "Play Audio", "Originate Call").
2.  **Connecting Steps**: Drag from a node's source handle (right side) to another node's target handle (left side).
    *   **Events**: Different handles represent different events (e.g., "Answered", "Hangup").
3.  **Configuration**: Click a node to open the **Config Panel** on the right.
    *   Set parameters like `Caller ID`, `Audio File Path`, or `Webhook URL`.
    *   Add comments to document your logic.
4.  **Testing**:
    *   Use the **Demo Workflows** to see examples of complex routing.
    *   Click **Export JSON** to get the raw configuration for your backend.

