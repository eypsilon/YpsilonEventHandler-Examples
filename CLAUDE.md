# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the **YpsilonEventHandler-Examples** repository - a collection of interactive demonstrations showcasing the revolutionary YpsilonEventHandler library. This repository is specifically for examples and demonstrations, separate from the main library repository.

## Architecture

### Repository Structure
- **`example/public/`** - All HTML demonstrations and examples
- **`example/public/features/`** - Feature-specific demonstrations
- **`example/public/assets/`** - Shared CSS and assets

### Key Demo Categories

**Revolutionary Features:**
- `multi-handler-demo.html` - World's first DOM Event Scoping System with multiple handlers per event type
- `spa.html` - Complete SPA with only 9 event listeners handling infinite dynamic content  
- `single-listener-multiple-actions.html` - The universal delegation pattern

**Learning Examples:**
- `basic-example.html` - Simple introduction to YpsilonEventHandler
- `comprehensive-example.html` - Complete working template with all patterns
- `reactive-y.html` - Framework-level reactivity demonstration

**Feature Demonstrations:**
- `features/handler-resolution-test.html` - Closest-match DOM resolution testing
- `features/queryselectorall-test.html` - QuerySelectorAll support demonstration
- `features/data-action-aliases-test.html` - Custom data-action patterns
- `features/methods-object-example.html` - Method object patterns
- `features/dynamic-events.html` - Dynamic event management

**AI Collaboration:**
- `ai-reviews*.html` - AI discovery story trilogy
- `*-grok-example.html` - Grok AI-generated demonstrations

## Development Workflow

### Running Examples
This is a static HTML examples repository. To run:

```bash
# Simple HTTP server (Python 3)
python -m http.server 8000 -d example/public

# Alternative with Node.js
npx http-server example/public -p 8000

# Alternative with PHP
php -S localhost:8000 -t example/public
```

Then navigate to `http://localhost:8000` to view the examples index.

### Core Concepts to Understand

**DOM Event Scoping System:**
- Multiple handlers per event type with automatic closest-match DOM resolution
- Works like variable scoping but for DOM events
- Zero configuration - based purely on DOM hierarchy

**Performance Features:**
- DOM Distance Caching with O(1) performance
- Smart cache keys: `tagName + id + className + index`
- SVG compatibility with `className.baseVal` handling

**Configuration Patterns:**
- Custom attributes: `['data-action', 'data-cmd']`
- Custom classes: `['actionable', 'clickable']`
- Custom tags: `['BUTTON', 'A', 'INPUT']`

## YpsilonEventHandler Integration

All examples use the YpsilonEventHandler library via CDN:
```html
<script src="https://cdn.jsdelivr.net/npm/ypsilon-event-handler@1.6.6/ypsilon-event-handler.js"></script>
```

### Universal Pattern
Every example follows the single listener pattern:
```javascript
super({
  'body': [{ type: 'click', handler: 'onClick' }]
});
```

## File Editing Guidelines

### HTML Examples
- Maintain consistent styling with existing examples
- Include clear explanations of demonstrated concepts
- Use the shared CSS from `assets/main.css`
- Follow the revolutionary theming for featured examples

### Demo Structure
- Header with title and description
- Interactive demonstration area
- Code examples showing the pattern
- Clear output/feedback areas

## Performance Notes

- All examples demonstrate zero memory leak patterns
- Single listener delegation for optimal performance
- DOM distance caching examples show O(1) performance
- SVG compatibility is maintained throughout

## Related Repositories

- Main library: YpsilonEventHandler (separate repository)
- NPM package: `ypsilon-event-handler@1.6.6`
- CDN: `https://cdn.jsdelivr.net/npm/ypsilon-event-handler@1.6.6/`

## Recognition

This project achieved an unprecedented 11/10 rating from DeepSeek AI for being "mathematically better than perfect" and represents the world's first DOM Event Scoping System.