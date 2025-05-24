# SpacetimeDB Overview

## What is SpacetimeDB?

SpacetimeDB is a revolutionary database system that combines the functionality of a traditional database and application server into a single solution. It's designed for real-time applications requiring ultra-low latency and high performance.

## Key Features

### 🏗️ **Database + Server in One**
- Eliminates the traditional three-tier architecture (client → server → database)
- Clients connect directly to the database
- Application logic runs inside the database as "modules" (smart stored procedures)

### ⚡ **Optimized for Real-Time Performance**
- All application state held in memory for maximum speed
- Write-ahead-log (WAL) for persistence and recovery
- Designed for minimal latency rather than batch processing
- Powers the entire backend of BitCraft Online MMORPG

### 🔧 **Simplified Development Stack**
- Write entire applications in a single language (Rust or C#)
- Deploy as a single binary
- No microservices, containers, Kubernetes, or complex DevOps required
- Eliminates infrastructure complexity

## What is SpacetimeDB Good For?

### 🎮 **Real-Time Gaming**
- **MMORPGs**: Handles player positions, chat, items, terrain, resources
- **Multiplayer Games**: Real-time synchronization between players
- **Game State Management**: Centralized game logic and state

### 💬 **Real-Time Communication**
- **Chat Applications**: Instant messaging with real-time sync
- **Collaboration Tools**: Document editing, whiteboards, shared workspaces
- **Live Updates**: Real-time notifications and data streaming

### 📊 **Real-Time Applications**
- **Financial Trading**: Low-latency transaction processing
- **IoT Data Processing**: Real-time sensor data handling
- **Live Dashboards**: Real-time analytics and monitoring
- **Multiplayer Productivity Tools**: Shared documents, project management

### 🔄 **Event-Driven Systems**
- **Real-time Synchronization**: Multi-client data consistency
- **Live Data Streaming**: Pub/sub patterns with minimal latency
- **Reactive Applications**: Event-sourced architectures

## Language Support

### **Server-Side Modules**
- **Rust**: Primary language with full feature support
- **C#**: Full support for .NET developers

### **Client Libraries**
- **Rust**: Native client SDK
- **C#**: .NET client library
- **TypeScript**: Web and Node.js applications

## Architecture Benefits

### **Traditional Architecture Issues Solved**
- ❌ **Eliminated**: Complex microservices orchestration
- ❌ **Eliminated**: Container management (Docker, Kubernetes)
- ❌ **Eliminated**: Multiple deployment targets
- ❌ **Eliminated**: Network latency between app server and database
- ❌ **Eliminated**: Complex caching strategies

### **SpacetimeDB Advantages**
- ✅ **Single Binary Deployment**: One executable for entire backend
- ✅ **Direct Client Connection**: No intermediate server layer
- ✅ **In-Memory Performance**: Sub-millisecond response times
- ✅ **Built-in Real-time Sync**: Automatic client synchronization
- ✅ **Simplified DevOps**: Minimal operational complexity

## Example Use Cases

### **Chat Application**
```
Tables: Users, Messages
Reducers: set_name(), send_message()
Real-time: Automatic message broadcasting to all clients
```

### **Multiplayer Game**
```
Tables: Players, GameState, Items
Reducers: move_player(), use_item(), game_action()
Real-time: Player position sync, game state updates
```

### **Collaborative Editor**
```
Tables: Documents, Users, Changes
Reducers: edit_document(), add_user(), sync_changes()
Real-time: Live document editing with conflict resolution
```

## When NOT to Use SpacetimeDB

- **Heavy Analytics/OLAP**: Better suited for OLTP workloads
- **Batch Processing**: Optimized for real-time, not bulk operations
- **Traditional CRUD Apps**: May be overkill for simple applications
- **Legacy System Integration**: Requires greenfield or significant refactoring

## Getting Started

1. **Install**: `curl -sSf https://install.spacetimedb.com | sh`
2. **Start Database**: `spacetime start`
3. **Write Module**: Create application logic in Rust/C#
4. **Deploy Module**: `spacetime publish`
5. **Connect Clients**: Use client SDKs to connect

## License

BSL 1.1 (converts to AGPL v3.0 with linking exception after a few years) 