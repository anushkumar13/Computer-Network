# What is Caching?

**Caching** means storing copies of files in a temporary location called a **cache** so that they can be accessed quickly. In technical terms, a cache is any temporary storage area where copies of data or files are kept. Most commonly, the term is used in the context of internet technology.

For example, web browsers cache HTML files, JavaScript, images, and other resources so that websites load faster. Similarly, DNS servers cache DNS records for quick domain name lookups. Content Delivery Network (CDN) servers also cache content to reduce latency, which means minimizing delays in data delivery.

---

## How Does Caching Work?

To understand caching, consider a real-life example. When explorer Roald Amundsen was returning from the South Pole in 1912, he and his team used food caches (stored supplies) along the route. This way, they did not have to wait for supplies from the base camp every time, making their journey much more efficient.

Internet caching works similarly—it temporarily stores content so that users can browse the web faster without downloading everything repeatedly.

---

## What Does Browser Cache Do?

Whenever a user opens a webpage, the browser needs to download a lot of data to display that page. To reduce page load time, the browser caches much of this content by saving copies on the user’s device (hard drive or storage).

Next time the user visits the same page, most of the content is already stored locally, so the page loads much faster.

The browser keeps these cached files until their **TTL (Time To Live)** expires or the cache storage on the device becomes full. TTL is the duration for which the content should be kept in the cache.

If the user wants, they can manually clear their browser cache to free up space or remove outdated data.

---

# What is CDN Caching?

**CDN** stands for **Content Delivery Network**. It is a network that caches content—such as images, videos, or webpages—on proxy servers. These proxy servers are located closer to the users, meaning they are physically nearer than the origin servers, which store the original content.

A **proxy server** is a server that receives requests from clients (users or devices) and then forwards those requests to the origin servers.

Since CDN proxy servers are closer to users, they can deliver content much faster.

---

## Example of CDN

Think of a CDN like a chain of grocery stores. If you want to buy vegetables, you don’t travel all the way to the farm, which is far away. Instead, you go to your local grocery store, which is much closer. The grocery store has vegetables that came from the farm, so you get your vegetables within minutes or seconds, not days.

Similarly, a CDN caches internet content (like webpages) in its proxy servers (like grocery stores), which are closer to the users than the origin server (the farm). This way, webpages load much faster.

---

## How Does CDN Caching Work?

When a user requests content from a CDN-enabled website, the CDN first fetches the content from the origin server. Then, it caches a copy of this content on its proxy servers for future requests.

As long as users keep requesting that content, the CDN keeps the cached copy on its servers to deliver it quickly next time.

---

# What is CDN Cache Hit?

A **cache hit** occurs when a client device (the user’s device) requests certain content, and that content is already stored in the cache. This means the CDN’s proxy server already has the content ready.

Because of this, the content loads very quickly since the CDN can deliver it immediately without contacting the origin server.

---

# What is Cache Miss?

A **cache miss** happens when the requested content is **not** available in the cache. In other words, the cache cannot fulfill the user’s request.

In this case, the CDN server forwards the request to the origin server. Once the CDN receives the content from the origin server, it saves a copy in its cache so that future requests for the same content result in a cache hit, allowing faster delivery.

---

**Summary:**

- **Cache Hit:** Content is found in the cache → fast delivery to user.  
- **Cache Miss:** Content not found in the cache → CDN fetches from origin server, caches it, then delivers.

---

# CDN Caching Servers and Their Global Distribution

CDN caching servers are located in data centers spread across different places around the world. For example, Cloudflare has CDN servers in over **330 cities worldwide**, ensuring these servers are physically close to users.

These locations where CDN servers are placed are called **data centers**. Because CDN servers are near to users geographically, they can deliver content much faster.

This global distribution of CDN servers helps reduce latency and improves the overall speed of content delivery to users everywhere.

---

# TTL (Time To Live) in CDN Caching

When websites send content to CDN servers, they also send a value called **TTL**, which stands for **Time To Live**. TTL indicates how long the content should remain cached on the CDN server.

This TTL value is stored inside the **HTTP header** and specifies the duration (in seconds, minutes, or hours) for which the content will be kept in the cache.

Once the TTL expires, the cached content is removed from the CDN server automatically.

Additionally, some CDNs may remove cached content earlier if:
- The content has not been requested for a long time, or
- The CDN customer manually purges (deletes) the content from the cache.

This mechanism ensures that users get fresh content and the cache storage is efficiently managed.

---

# DNS Caching

DNS caching happens on DNS servers. When a domain's IP address needs to be resolved, the DNS server first stores recent DNS lookups in its cache. This means if the IP address of a domain is already in the cache, the DNS server does not need to query the authoritative nameservers every time. It can quickly provide the IP address from its cache.

This speeds up domain access on the internet because the server answers from cache instead of repeatedly asking external servers.

# Search Engine Caching

Search engines also perform their own caching. They store cached copies of frequently appearing webpages in their search results. This helps in cases when the original website is temporarily down or unresponsive.

In such situations, the search engine can serve the cached copy to the user, ensuring no interruption in accessing the needed content. This type of caching acts like a backup, improving user experience by providing faster and reliable access to information.

---

# Cloudflare CDN Caching

Cloudflare provides caching services through its CDN, which has 330 Points of Presence (PoPs) spread worldwide. These PoPs are essentially data centers located close to users to ensure faster content delivery.

Cloudflare offers a free CDN caching plan that includes basic caching. Customers on paid plans can customize their caching strategies, meaning they can decide how long specific content stays in the cache or how it gets updated.

## Anycast Technology

Cloudflare's network uses **Anycast technology**, which allows the same content to be delivered from any Cloudflare data center worldwide. For example, a user in London and another in Sydney will receive content from their nearest CDN servers, located just a few miles away.

This results in very fast content delivery, reduced latency, and a smoother user experience.

## Summary

In simple terms, Cloudflare caching stores your website content on servers close to your users, enabling quick loading of content regardless of where the user is located globally. This is all made possible by Cloudflare's extensive global network and the power of Anycast technology.

---

