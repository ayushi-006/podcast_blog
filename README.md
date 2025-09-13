# Podcast-to-Blog Transformer

> Transform your spoken words into compelling written content with the power of AI

## What It Does

This intelligent pipeline takes raw audio or video files and transforms them into polished, engaging blog posts. Whether you've recorded a lecture, interview, or casual conversation, this tool extracts the essence and restructures it into readable, SEO-friendly content.

**The Magic Behind the Curtain:**
1. **Audio Extraction & Compression** - Automatically processes video files and compresses audio to meet API requirements
2. **Speech-to-Text Transcription** - Leverages OpenAI's Whisper model for accurate transcription
3. **Intelligent Content Generation** - Uses GPT-4 to transform raw transcripts into structured, narrative-driven blog posts

## Quick Start

### Prerequisites
```bash
pip install openai pydub
```

### Environment Setup
Create a `.env` file with your OpenAI API key:
```
OPENAI_API_KEY=your_api_key_here
```

### Usage
1. Open `podcast.ipynb` in Jupyter Notebook or VS Code
2. Replace the file path with your audio/video file
3. Run all cells to get your generated blog post

The pipeline will:
- Process and compress your media file
- Generate a transcription
- Create a polished blog post saved as `generated_blog_post.md`

## Technical Architecture

**Audio Processing Pipeline:**
- Extracts audio from video files (.mkv, .mp4, etc.)
- Compresses to 8kHz mono audio at 32k bitrate
- Ensures files meet OpenAI's 25MB API limit

**Content Intelligence:**
- Uses Whisper-1 model for transcription accuracy
- Employs GPT-4 with specialized prompts for educational content
- Implements retry logic for API reliability
- Generates 700-word structured blog posts

**File Structure:**   
```
podcast_blog/
├── podcast.ipynb           # Main processing pipeline
├── results/ 
├   ├──transcription_result.txt
├   ├──generated_blog_post.md
└── README.md             # You are here
```
## Current Limitations

- Optimized for educational content (Electronics programs)
- Maximum file size limited by OpenAI API constraints
- Requires manual file path updates
- Single-threaded processing

## Contributing

This project represents the foundation of a more comprehensive content automation system. The architecture is designed to be extensible, with clear separation between audio processing, transcription, and content generation phases.


---

**Perfect for:** Content creators, educators, researchers, and anyone who wants to repurpose spoken content into written format without losing the essence and engagement of the original material.
