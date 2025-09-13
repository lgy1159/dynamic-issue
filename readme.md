Here's a concise English description of your problem for Dynamic support:

## Issue Title
**ZeroDev Multi-Chain RPC Configuration Not Working - Custom RPC URLs Ignored**

## Issue Description

I'm experiencing an issue with ZeroDev multi-chain support where custom RPC URLs are not being respected. I need to configure ZeroDev to use specific RPC endpoints for different chains without setting them in the ZeroDev dashboard.

### Problem
When using ZeroDev with Dynamic SDK, the `setBalance` method consistently calls an unexpected default RPC URL instead of my configured custom RPC URLs, regardless of which configuration approach I use.

### Attempted Solutions
I've tried three different approaches to configure custom RPC URLs:

1. **Dynamic Chains & Networks Tab Configuration** - Added custom RPC URLs in the `evmNetworks` configuration within DynamicContextProvider settings
2. **ZeroDevSmartWalletConnectorsWithConfig** - Used the config parameter to dynamically assign RPC URLs during `switchNetwork` operations  
3. **Wagmi Provider Setup** - Configured custom transports in wagmi config and wrapped the app with DynamicWagmiConnector

### Current Behavior
All three approaches fail to override the RPC URLs. ZeroDev continues to use the same default RPC endpoint across all chains, ignoring my custom configuration entirely.

### Expected Behavior
ZeroDev should respect the custom RPC URLs I've configured and use them for blockchain interactions instead of falling back to default endpoints.

### Environment
- Using Dynamic SDK with ZeroDev integration
- Supporting multiple chains: Ethereum, BNB Smart Chain, Polygon
- Next.js application
- Need to avoid ZeroDev dashboard RPC configuration

### Questions
Is there a specific configuration hierarchy or additional setup required to make ZeroDev respect custom RPC URLs in a multi-chain Dynamic integration? The documentation doesn't clearly address this scenario for production environments where dashboard configuration isn't preferred.

---

This version focuses purely on describing the problem without code examples, making it suitable for submitting to Dynamic's support channels.
