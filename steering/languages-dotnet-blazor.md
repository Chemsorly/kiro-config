# Blazor Rules
## Purpose
Blazor-specific development guidelines, component lifecycle management, and UI best practices.

## Component Lifecycle
- Use proper Blazor component lifecycle for accessibility features (OnAfterRenderAsync for DOM updates) (ID: BLAZOR_ACCESSIBILITY_LIFECYCLE)
- Move JavaScript interop calls from OnInitializedAsync to OnAfterRenderAsync to avoid prerendering issues (ID: BLAZOR_JAVASCRIPT_LIFECYCLE)
- Implement proper disposal patterns (IDisposable, DisposeAsync) for component cleanup (ID: BLAZOR_COMPONENT_DISPOSAL)
- Use StateHasChanged() after async operations in OnAfterRenderAsync for UI updates (ID: BLAZOR_STATE_MANAGEMENT)

## JavaScript Interop
- Handle InvalidOperationException for prerendering scenarios when JavaScript is unavailable (ID: BLAZOR_PRERENDERING_HANDLING)
- Ensure JavaScript interop calls don't break screen reader functionality (ID: BLAZOR_ACCESSIBILITY_INTEROP)
- Optimize JavaScript interop calls by batching operations and avoiding frequent DOM updates (ID: BLAZOR_JAVASCRIPT_OPTIMIZATION)
- Use direct DOM manipulation with JavaScript event listeners when Blazor event binding conflicts occur (ID: BLAZOR_DOM_MANIPULATION)

## Event Handling
- Avoid conflicts between @bind, @onchange, and @bind:after patterns (ID: BLAZOR_EVENT_BINDING_CONFLICTS)
- Use pure JavaScript event listeners for complex UI interactions when Blazor binding fails (ID: BLAZOR_JAVASCRIPT_EVENTS)
- Implement proper focus management and visual focus indicators (ID: BLAZOR_FOCUS_MANAGEMENT)

## Accessibility
- Provide proper semantic HTML structure with appropriate ARIA labels (ID: BLAZOR_SEMANTIC_HTML)
- Ensure keyboard navigation support for all interactive elements (ID: BLAZOR_KEYBOARD_NAVIGATION)
- Implement proper focus management and visual focus indicators (ID: BLAZOR_FOCUS_MANAGEMENT)
- Use proper button vs link semantics based on functionality (ID: BLAZOR_SEMANTIC_ELEMENTS)
- Implement accessible dropdown and modal components (ID: BLAZOR_ACCESSIBLE_COMPONENTS)
- Provide clear status messages for dynamic content updates (ID: BLAZOR_STATUS_MESSAGES)
- Implement accessible form validation with clear error messages (ID: BLAZOR_ACCESSIBLE_VALIDATION)
- Provide accessible loading states and progress indicators (ID: BLAZOR_LOADING_STATES)

## UI Performance
- Minimize Blazor component re-rendering with proper state management (ID: BLAZOR_RENDERING_OPTIMIZATION)
- Use CSS variables for theme switching to avoid JavaScript DOM manipulation (ID: BLAZOR_CSS_VARIABLES)
- Implement efficient visual testing with headless browsers and screenshot caching (ID: BLAZOR_VISUAL_TESTING)

## Session Management
- Use HTTP connection ID for session tracking in Blazor Server applications (ID: BLAZOR_SESSION_TRACKING)
- Implement session-based resource tracking to prevent resource accumulation (ID: BLAZOR_SESSION_RESOURCES)

## Testing
- Use visual testing with Playwright screenshots for UI validation (ID: BLAZOR_VISUAL_TESTING_VALIDATION)
- Test component lifecycle methods with proper mocking (ID: BLAZOR_LIFECYCLE_TESTING)
- Create TestableComponent classes that override virtual methods for testing (ID: BLAZOR_TESTABLE_COMPONENTS)

## Priority
Medium

## Error Handling
- Handle JavaScript interop failures gracefully with fallback options
- Implement proper error boundaries for component failures
- Document Blazor-specific issues and solutions in lessons-learned