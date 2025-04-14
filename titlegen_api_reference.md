# TitleGen AI API – Reference Documentation

## Overview

The TitleGen API allows you to generate YouTube-optimized video titles based on a short prompt or video description. This endpoint uses Claude-based prompt logic to return catchy, SEO-friendly title suggestions.

## Base URL

```
https://api.titlegenai.io/v1
```

## Endpoint: Generate Titles

`POST /generateTitle`

### Description:
Generates 5–10 optimized YouTube titles for a given topic or description.

### Request

**Headers**
```http
Authorization: Bearer YOUR_API_KEY  
Content-Type: application/json
```

**Body**
```json
{
  "topic": "Silent vlogging and Gen Z aesthetic",
  "style": "casual",
  "platform": "YouTube",
  "tone": "relatable"
}
```

### Response

**Success (200 OK)**
```json
{
  "titles": [
    "Why Gen Z is Obsessed with Silent Vlogs",
    "Romanticizing Life Without Saying a Word",
    "The Quiet Revolution of Gen Z Aesthetic Vlogging",
    "POV: Your Life is a Vlog (With No Talking)",
    "Silent Vlogging is the New Main Character Energy"
  ]
}
```

**Error (400 Bad Request)**
```json
{
  "error": "Missing required field: topic"
}
```

## Usage Notes

- Maximum 100 characters per title
- API is optimized for short-form content ideas
- For tone customization, use values like: "funny", "dramatic", "educational", "edgy"

## Version

`v1.0` (Last updated: April 2025)
