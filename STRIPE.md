# Assignment 1: Stripe Subscription Integration

## Overview

Build a subscription management system with Stripe integration featuring monthly and yearly subscription plans. Users should be able to subscribe, view active subscriptions, and cancel subscriptions.

## Requirements

### Core Features

1. **Subscription Plans**

   - Monthly Plan: $25/month
   - Yearly Plan: $250/year
   - Display both plans with clear pricing

2. **Stripe Integration**

   - Integrate Stripe Checkout for payments
   - Handle successful and failed payments
   - Implement webhook handling for subscription events
   - Use Stripe test mode

3. **Subscription Management**

   - View active subscriptions
   - Cancel existing subscriptions
   - Handle subscription status changes (active, canceled, past_due)
   - Display subscription details (plan, status, next billing date)

4. **Data Storage**
   - Store subscription data in localStorage OR
   - Hard-code mock data with state management
   - Persist user subscription state across page refreshes

### UI/UX Requirements

- Clean, modern design using Shadcn/ui components
- Loading states during payment processing
- Success/error notifications
- Subscription status indicators

## Technical Specifications

### Required Pages/Components

1. **Pricing Page** (`/pricing`)

   - Display subscription plans
   - "Subscribe" buttons for each plan

2. **Subscription Dashboard** (`/dashboard`)

   - List active subscriptions
   - Subscription details (plan, status, billing date)
   - Cancel subscription functionality

3. **Payment Success/Cancel Pages**
   - `/payment/success` - Confirmation page
   - `/payment/cancel` - Cancellation page

### Stripe Setup

```bash
# Required environment variables
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_...
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
```

### Mock Data Structure (if using hard-coded data)

```typescript
interface Subscription {
  id: string;
  planId: "monthly" | "yearly";
  status: "active" | "canceled" | "past_due";
  currentPeriodStart: Date;
  currentPeriodEnd: Date;
  cancelAtPeriodEnd: boolean;
  amount: number;
  currency: string;
}
```

## Implementation Guidelines

### Stripe Integration Steps

1. Set up Stripe SDK and configure API keys
2. Create product and price objects in Stripe Dashboard
3. Implement Checkout Session creation
4. Handle webhook events (subscription created, updated, deleted)
5. Manage subscription lifecycle

### File Structure Suggestion

```
src/
├── app/
│   ├── pricing/
│   │   └── page.tsx
│   ├── dashboard/
│   │   └── page.tsx
│   ├── payment/
│   │   ├── success/page.tsx
│   │   └── cancel/page.tsx
│   └── api/
│       ├── create-checkout-session/
│       ├── cancel-subscription/
│       └── webhooks/
├── components/
│   ├── SubscriptionCard.tsx
│   ├── PricingPlan.tsx
│   └── SubscriptionManager.tsx
├── lib/
│   ├── stripe.ts
│   └── subscription-utils.ts
└── types/
    └── subscription.ts
```

## Test Cards (Stripe Test Mode)

- **Success**: 4242 4242 4242 4242
- **Decline**: 4000 0000 0000 0002
- Use any future expiry date and any CVC

## Deliverables

1. Complete Next.js application
2. Stripe integration working in test mode
3. All core features functional
4. Error handling implemented

## Testing

- Use Stripe test cards for payments
- Webhook testing with Stripe CLI (optional)

```
Remember to focus on code quality, user experience, and proper error handling. Good luck!
```
