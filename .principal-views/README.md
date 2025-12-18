# Bun Runtime Architecture

This directory contains Principal View CLI configuration files that document the Bun JavaScript runtime architecture.

## Files

- `library.yaml` - Defines component types and relationships used in the architecture
- `architecture.canvas` - Visual graph showing how different components interact
- `.privurc.yaml` - Lint configuration for validation rules

## Architecture Overview

The graph visualizes the key components of Bun:

### Core Runtime

- **Runtime** - Main orchestrator for the Bun runtime
- **JavaScriptCore** - WebKit's JavaScript execution engine
- **EventLoop** - Coordinates asynchronous operations

### Build Pipeline

- **JS Parser** - Parses JavaScript/TypeScript source code
- **Transpiler** - Transforms and transpiles code
- **Bundler** - Bundles modules with tree-shaking
- **Package Manager** - npm-compatible dependency management

### APIs and Compatibility

- **Node.js API** - Node.js compatibility layer
- **Web API** - Standard web APIs (Fetch, Streams, etc.)
- **Bun API** - Bun-specific extensions and APIs

### Network Layer

- **HTTP Server** - HTTP server implementation
- **HTTP Client** - HTTP client for fetch requests
- **WebSocket** - WebSocket client implementation

## Commands

- `npx @principal-ai/principal-view-cli validate` - Validate all configuration files
- `npx @principal-ai/principal-view-cli doctor` - Check project setup
- `npx @principal-ai/principal-view-cli lint` - Lint configuration (if additional canvas files are added)

## Component Relationships

The graph shows several types of relationships:

- **Parses/Transpiles/Bundles** - Code flow through the build pipeline
- **Executes** - Runtime executing JavaScript via JavaScriptCore
- **DependsOn** - Component dependencies
- **Implements** - API compatibility implementations
- **Extends** - Feature extensions
- **Communicates** - Inter-component communication

This architecture visualization helps understand how different parts of Bun work together to provide a complete JavaScript runtime and toolkit.
