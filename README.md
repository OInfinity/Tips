# LearnFast
Methods
## Step 1
- Watch if it is a Video
- Listen if it is an Audio
- Read if it is written
### POV :
`Do that first, so that you can have an idea of your next move during your lab/practice.`
- You might not have any idea of what you are watching, listening to, or reading, and now you can be proud of yourself. That means your mind is expanding, and that is the whole point.
### Know this by heart

| Address           | Purpose                       | Notes                                                                     |
| ----------------- | ----------------------------- | ------------------------------------------------------------------------- |
| `127.0.0.1`       | Loopback / Local host         | Always the same, tests local network stack                                |
| `Default Gateway` | Router’s IP                   | Usually something like `192.168.x.x` or `10.x.x.x`, check with `ipconfig` |
| `8.8.8.8`         | Google Public DNS IP          | Reliable for testing internet connectivity (bypasses DNS)                 |
| `google.com`      | Domain to test DNS + internet | Common hostname for checking DNS resolution                               |

### purpose
| Address                                     | Reason to Ping It                                                                                                                                                                                       |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`127.0.0.1`**                             | To test your **own computer’s network stack** — confirms if your TCP/IP software and network adapter are working correctly. If this fails, the problem is local to your PC.                             |
| **`Default Gateway` (e.g., `192.168.1.1`)** | To check if your PC can reach the **local router or gateway** — confirms that your device is connected to the local network. If this fails, you likely have a cable/Wi-Fi or router connection problem. |
| **`8.8.8.8`**                               | To test if your PC can reach the **internet directly by IP**, bypassing DNS. If this fails but the Default Gateway ping works, your internet connection is down beyond the router.                      |
| **`google.com`**                            | To test both **DNS resolution** and internet connectivity. If `8.8.8.8` works but this fails, you have a DNS problem (your PC cannot resolve domain names).                                             |

###  Other common combinations:
✅ 127.0.0.1 ✅ Gateway ❌ 8.8.8.8 ❌ google.com
Local network OK, but internet is down.

✅ 127.0.0.1 ✅ Gateway ✅ 8.8.8.8 ❌ google.com

DNS issue — internet is reachable via IP but names can't be resolved.

✅ 127.0.0.1 ❌ Gateway ❌ 8.8.8.8 ❌ google.com

PC’s network stack is working, but not connected to router — check Wi-Fi or cable.

### Summary:
- 127.0.0.1: Is your PC’s network software okay?

- Default Gateway: Can your PC talk to the router?

- 8.8.8.8: Can your PC access the internet (IP level)?

- google.com: Can your PC resolve domain names and access the internet?
