<h1 align="center">📦 Baileys In-Memory Store</h1>

<p align="center">
  Single File • No TS • Fast • Simple • Baileys Ready
</p>

<hr/>

<h3>📖 Description</h3>
<p>
Lightweight in-memory store for <b>Baileys WhatsApp Library is memory based</b>.  
No TypeScript, no additional dependencies, just one package to use.
</p>

<h3>✨ Features</h3>
<ul>
  <li>📂 Chats, Messages, Contacts, Groups</li>
  <li>🧠 In-memory store (fast & light)</li>
  <li>🔄 Auto sync via <code>ev</code> Baileys</li>
  <li>💾 Save & Load JSON</li>
  <li>🏷️ Label & Label Association</li>
  <li>🟢 Presence tracking</li>
</ul>

<h3>🧩 Function</h3>
<ul>
  <li><code>bind(ev)</code> – bind event Baileys</li>
  <li><code>loadMessages(jid, count, cursor?)</code></li>
  <li><code>loadMessage(jid, id)</code></li>
  <li><code>mostRecentMessage(jid)</code></li>
  <li><code>fetchImageUrl(jid, sock?)</code></li>
  <li><code>fetchGroupMetadata(jid, sock?)</code></li>
  <li><code>getLabels()</code></li>
  <li><code>getChatLabels(chatId)</code></li>
  <li><code>getMessageLabels(messageId)</code></li>
  <li><code>writeToFile(path)</code></li>
  <li><code>readFromFile(path)</code></li>
  <li><code>writeToFileSqlite(path)</code></li>
  <li><code>readFromFileSqlite(path)</code></li>
  <li><code>writeToFileAuto(path)</code></li>
  <li><code>readFromFileAuto(path)</code></li>
</ul>

<h3>🚀 How to Use</h3>

<pre><code class="language-js">

import InMemoryStore from "baileys-inmemory-store"
import baileys from "baileys"

const sock = baileys.makeWASocket({
  // config
})

const store = InMemoryStore()
store.bind(sock.ev)

// take the last message
const msg = store.mostRecentMessage(jid)

// load some messages
store.loadMessages(jid, 20)

// load 1 message
store.loadMessage(jid, messageId)
</code></pre>

<h3>💾 Save / Load ( JSON )</h3>

<pre><code class="language-js">
store.writeToFile("./store.json")
store.readFromFile("./store.json")
</code></pre>

<h3>💾 Save / Load ( Sqlite )</h3>

<pre><code class="language-js">
store.writeToFileSqlite("./store.db")
store.readFromFileSqlite("./store.db")
</code></pre>

<h3>💾 Save / Load ( AUTO )</h3>

<pre><code class="language-js">
store.writeToFileAuto("./store.json")
// Or
store.writeToFileAuto("./store.db")

store.readFromFileAuto("./store.json")
// Or
store.readFromFileAuto("./store.db")
</code></pre>

<h3>👤 Credit</h3>
<p>
<b>FgsiDev</b><br/>
Built for Baileys WhatsApp ecosystem
</p>

<hr/>

<p align="center">
  ⚡ Simple • Brutal • Works
</p>
