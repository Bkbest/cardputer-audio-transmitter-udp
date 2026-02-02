# Cardputer Audio Transmitter UDP

A powerful audio recording and transmission application for M5Stack Cardputer that enables voice-based calendar management through AI integration.

## Resources

- [UIFlow Project Page](https://uiflow2.m5stack.com/?pkey=f4da1d7386ed49ea977130ec68e813f2)
- [Calendar AI Agent Repository](https://github.com/Bkbest/calendar-agent)
- [M5Stack Cardputer Documentation](https://docs.m5stack.com/en/core/cardputer)

## What is Cardputer?

The M5Stack Cardputer is a compact, portable computing device featuring a built-in keyboard, display, and various connectivity options. It's designed for IoT projects, prototyping, and mobile computing applications. This particular application leverages the Cardputer's audio capabilities to create a voice-activated calendar management system.

## Features

- **15-Second Audio Recording**: Record voice memos up to 15 seconds long
- **UDP Audio Transmission**: Send recorded audio to any listening UDP server
- **Simple Controls**: Intuitive button-based interface for recording, playback, and transmission
- **AI Calendar Integration**: Works seamlessly with the Calendar AI Agent for intelligent task management

## How to Use

### Basic Controls

1. **Start Recording**: Click the Go button once to begin recording audio
2. **Playback Recording**: Hold the Go button to play back your recorded audio
3. **Transmit Audio**: Press the Spacebar to submit the recorded audio for transmission
4. **Re-record**: Click the Go button again to record a new sample if you're not satisfied with the current one

### Operation Flow

```
1. Press Go (click) → Start 15-second recording
2. Hold Go → Review recorded audio
3. Press Spacebar → Transmit to UDP server
4. Repeat → Record new sample if needed
```

## AI Calendar Agent Integration

When combined with the [Calendar AI Agent](https://github.com/Bkbest/calendar-agent), this Cardputer app becomes a powerful AI note-taking assistant that can:

- **Create Calendar Events**: Automatically schedule tasks and reminders
- **Set Recurring Reminders**: Establish daily or periodic check-ins
- **Research Resources**: Find relevant articles and videos for your tasks
- **Smart Task Management**: Organize your schedule with AI assistance

### Example Usage

**Voice Command**: *"Create a recurring reminder everyday for 7 days to learn Python, new topic everyday, tag some useful resources or videos in the summary."*

**AI Agent Response**:
- Creates a 7-day recurring calendar event
- Assigns different Python topics for each day
- Researches and attaches relevant tutorials, articles, and videos
- Provides a comprehensive learning plan with resources

### AI Agent Capabilities

The Calendar AI Agent provides:

- **Natural Language Processing**: Understands complex voice commands
- **Intelligent Scheduling**: Finds optimal time slots based on your calendar
- **Resource Curation**: Searches for and attaches relevant learning materials
- **Multi-calendar Support**: Manages events across different calendar systems
- **Context Persistence**: Maintains conversation history and preferences

## Technical Architecture

### Cardputer App
- Audio recording and playback functionality
- UDP client for audio transmission
- Simple button-based user interface
- 15-second recording limit

### Calendar AI Agent
- **UDP Server**: Listens on port 9876 for audio packets
- **Audio Processing**: Converts and transcribes speech using Eleven Labs API
- **LangGraph Agent**: Orchestrates calendar management workflows
- **Calendar Integration**: Connects to Google Calendar API
- **Search Integration**: Uses Tavily search for resource discovery

## Setup Instructions

### Cardputer Setup
1. Load the audio transmitter app onto your Cardputer device
2. Ensure the device is connected to your network
3. Configure the UDP server IP address in the app settings

### Calendar AI Agent Setup
1. Clone the Calendar AI Agent repository:
   ```bash
   git clone https://github.com/Bkbest/calendar-agent
   ```

2. Install dependencies:
   ```bash
   cd calendar-agent
   pip install -r requirements.txt
   ```

3. Configure API keys:
   - Eleven Labs API key for speech transcription
   - Tavily API key for web search
   - Google Calendar API credentials

4. Run the UDP server:
   ```bash
   cd src
   python udp_audio_server.py
   ```

The server will start listening on port 9876 for audio input from your Cardputer.

## Use Cases

### Personal Productivity
- Quick voice notes that become calendar events
- Meeting reminders with automatic resource gathering
- Learning schedules with curated content

### Education
- Study plan creation with resource links

## Requirements

### Hardware
- M5Stack Cardputer device
- Network connectivity (WiFi)

### Software
- Calendar AI Agent server
- API keys for:
  - Eleven Labs (speech transcription)
  - Tavily (web search)
  - Google Calendar API

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs and feature requests.

---

Transform your voice into organized, actionable calendar events with the power of AI!
