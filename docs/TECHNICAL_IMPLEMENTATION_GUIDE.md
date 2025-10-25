# AI Requirements Extractor - Technical Implementation Guide

## Architecture Overview

### Component Stack

### Technology Stack
- **Frontend Framework:** React 18+
- **Language:** TypeScript/JavaScript
- **Styling:** Tailwind CSS
- **AI Provider:** Anthropic Claude API
- **Components:** Lucide React Icons
- **Charts:** Recharts (optional)

## Sample Implementation

### Sample Data Structure
```typescript
interface Sample {
  id: string;
  name: string;
  category: 'ecommerce' | 'healthcare' | 'fleet' | 'banking' | 'saas' | 'iot';
  complexity: 'medium' | 'high' | 'very-high';
  description: string;
  text: string;
  expectedRequirements: number;
}

const samples: Record<string, Sample> = {
  ecommerce: {
    id: 'ecommerce',
    name: '🛒 E-Commerce Platform',
    category: 'ecommerce',
    complexity: 'medium',
    description: 'Payment processing, inventory management, security',
    text: '...',
    expectedRequirements: 9
  },
  // ... more samples
};
```

### Sample Loading Function
```typescript
const loadSample = (sampleId: string) => {
  const sample = samples[sampleId];
  if (!sample) return;
  
  setSelectedSample(sampleId);
  setInput(sample.text);
  setExpectedCount(sample.expectedRequirements);
  setActiveTab('input');
};
```

### Extraction Function
```typescript
const extractRequirements = async () => {
  setLoading(true);
  setError(null);
  
  try {
    const response = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify({
        model: 'claude-sonnet-4-20250514',
        max_tokens: 2000,
        messages: [{
          role: 'user',
          content: `Extract business requirements from this text:\n\n${input}\n\nProvide structured requirements with type, priority, and description.`
        }]
      })
    });
    
    const data = await response.json();
    const extractedText = data.content[0].text;
    parseAndStoreRequirements(extractedText);
  } catch (err) {
    setError('Extraction failed: ' + err.message);
  } finally {
    setLoading(false);
  }
};
```

## Development Setup

### Prerequisites
```bash
Node.js 16+
npm or yarn
Git
GitHub account
```

### Installation
```bash
# Clone repository
git clone https://github.com/yourname/your-repo.git
cd your-repo

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Add your ANTHROPIC_API_KEY

# Start development server
npm run dev
# Visit http://localhost:3000
```

### Environment Variables

