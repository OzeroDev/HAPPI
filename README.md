# Fostering Positive Connections Through Interactive Messages: HAPPI

HAPPI is a system designed to foster emotional well-being and community connection through personalized, interactive messages in public spaces. Built as a robot-like device, HAPPI leverages Raspberry Pi, Python, REST APIs, and Bluetoothctl to enable users to share handwritten and digital messages, creating meaningful connections in natural settings.

## Research Overview Video
[Youtube Link](https://www.youtube.com/watch?v=U-ykGzghULk)

## Research Paper
See the full research paper: [HAPPI_paper.pdf](/HAPPI_paper.pdf)

## System Architecture

This repository contains the code for HAPPI, a monorepo containing three interconnected components that work together to create an interactive message-sharing experience:

### 1. Server (`/server`)
The core backend system hosted on a Raspberry Pi that orchestrates all HAPPI functionality:
- **Database Management**: Local MySQL database storing user messages and responses
- **Web Server**: Hosts the web interface and REST API endpoints
- **Printer Integration**: Multi-threaded printer management connecting to thermal and color printers via Bluetoothctl
- **Discord Bot**: Automated moderation system that notifies moderators of new submissions for verification
- **API Endpoints**: RESTful services for message submission, retrieval, and printing operations

### 2. Display (`/display`)
A Python-based display program that brings HAPPI to life with expressive animations:
- **Event Listener**: Self-hosted Flask server receiving events from the main server
- **Animation System**: Plays contextual video animations (blink, blush, grin, inquisitive, surprised) based on user interactions
- **Pygame Integration**: Full-screen display rendering optimized for the Raspberry Pi screen
- **Real-time Response**: Updates display dynamically in response to user actions (printing, submitting messages)

### 3. Web Interface (`/web`)
User-facing web application for message interaction:
- **Prompt Display**: Shows rotating prompts encouraging positive message sharing
- **Multi-modal Input**: Supports both text responses (up to 64 characters) and image uploads
- **Base64 Image Encoding**: Client-side image processing for seamless uploads
- **Responsive Design**: Optimized for iPad kiosk interface with background video
- **Real-time Feedback**: Immediate confirmation of message submissions

## How HAPPI Works

1. **Message Creation**: Users approach HAPPI and can write a handwritten message on the iPad or upload an image via QR code
2. **Moderation**: All submissions are automatically sent to Discord moderators for verification
3. **Animation Response**: HAPPI displays expressive animations (blush when receiving, grin when printing) to acknowledge interactions
4. **Message Printing**: Other users can print random messages created by previous users, receiving personalized tokens of positivity
5. **Community Building**: The cyclical interaction creates a "pay it forward" effect, spreading positivity through authentic human connection

## Key Features

- **Technology as Connector**: Facilitates human connection rather than replacing it
- **Authenticity**: Supports handwritten and personal messages for genuine interaction
- **Rewarding Positive Behavior**: Implements upstream reciprocity through message sharing
- **Community Connection**: Creates shared experiences through relatable peer stories
- **Exploration & Engagement**: Robot-like design with expressive animations invites curiosity
- **Self-Determination**: Empowers users to express themselves freely

## Deployment

HAPPI has been successfully deployed in real-world public settings with iterative improvements based on user feedback:
- Enhanced animations to strengthen connection between physical device and user interactions
- Improved engagement through expressive robot features (lights, animations, friendly interface)
- Cultural adaptation capabilities for different contexts (e.g., holiday-themed prompts)

## Technical Stack

- **Hardware**: Raspberry Pi, iPad kiosk, thermal printer, color printer
- **Backend**: Python, Flask, MySQL, REST APIs, Bluetoothctl
- **Frontend**: HTML, CSS, JavaScript, Base64 encoding
- **Display**: Pygame, OpenCV, video rendering
- **Moderation**: Discord Bot API

## Contributing to Mental Health & Well-being

HAPPI addresses the UN Sustainable Development Goal 3.4 (promote mental health and well-being) by:
- Combating loneliness through authentic in-person connections
- Providing opportunities for spontaneous acts of kindness
- Creating community in everyday public spaces
- Supporting emotional wellness through positive reinforcement

---

*Codebase developed entirely by Justin Mehes at the University of Minnesota*