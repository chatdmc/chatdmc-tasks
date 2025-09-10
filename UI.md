# Assignment 2: UI Design Implementation

## Overview

Implement a pixel-perfect UI design based on provided mockups. Focus on creating an interactive interface with functional components including tabs, accordions, and form elements.

## Design

[!Design To be Replicated](/WhatsApp%20-%20Live%20Chat.png)

## Requirements

### Core Features

1. **Exact Design Match**

   - Implement the provided design with pixel-perfect accuracy
   - Match colors, spacing, typography, and layout exactly

2. **Interactive Components**

   - **Tab Switching**: Functional tab navigation with active states
   - **Accordion**: Expandable/collapsible sections with smooth animations
   - **Form Elements**: Working textarea with basic send functionality
   - **Hover States**: Interactive hover effects on clickable elements

3. **No Rich Text Editor Required**
   - Use basic HTML textarea element
   - Simple send functionality (can be simulated)
   - Focus on design accuracy over complex functionality

## Technical Specifications

### Design Assets

- High-fidelity mockup image provided
- Extract colors, fonts, and measurements from the design
- Use browser dev tools to measure pixel-perfect spacing

### Required Interactions

1. **Tabs Component**

   ```typescript
   // Example tab structure
   const tabs = [
     { id: "tab1", label: "Overview", content: "..." },
     { id: "tab2", label: "Details", content: "..." },
     { id: "tab3", label: "Settings", content: "..." },
   ];
   ```

2. **Accordion Component**

   ```typescript
   // Example accordion structure
   const accordionItems = [
     {
       id: "item1",
       title: "Section Title",
       content: "Section content...",
       defaultOpen: false,
     },
   ];
   ```

3. **Form Functionality**
   - Basic textarea with placeholder text
   - Send button with onClick handler
   - Simple form state management

## Implementation Guidelines

### File Structure Suggestion

```
src/
├── app/
│   └── page.tsx
├── components/
│   ├── ui/           # Shadcn components
│   ├── TabsSection.tsx
│   ├── AccordionSection.tsx
│   ├── MessageForm.tsx
│   └── Layout.tsx
├── lib/
│   └── utils.ts
└── styles/
    └── globals.css
```

## Testing Requirements

1. Test all interactive elements
2. Validate form functionality

## Deliverables

1. Pixel-perfect implementation of the provided design
2. All interactive components working correctly
3. Clean, well-organized code

## Evaluation Focus

- **Design Accuracy**: How closely the implementation matches the provided design
- **Code Quality**: Clean, maintainable, and well-structured code
- **Functionality**: All interactive elements work as expected
- **User Experience**: Smooth interactions and appropriate feedback

Remember: The goal is not just to make it look similar, but to achieve pixel-perfect accuracy while maintaining excellent code quality and user experience. Good luck!
