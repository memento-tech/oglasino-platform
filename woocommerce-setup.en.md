# How to connect your WooCommerce shop to Oglasino

You have a web shop. Oglasino can show your products as listings, automatically. You set it up once, and after that your prices, photos and stock stay up to date on their own.

This guide walks you through everything, step by step. You don't need any technical knowledge — if you can use your WooCommerce admin page, you can do this.

If you get stuck at any point, write to us: **support@oglasino.com**.

## Contents

- [What is Shop Import?](#what-is-shop-import)
- [Before you start](#before-you-start)
- [Quick start](#quick-start)
- [Step 1: Prepare your WooCommerce store](#step-1-prepare-your-woocommerce-store)
- [Step 2: Connect your store on Oglasino](#step-2-connect-your-store-on-oglasino)
- [Step 3: The review](#step-3-the-review)
- [Step 4: Publish your products](#step-4-publish-your-products)
- [How syncing works](#how-syncing-works)
- [Adding new products later](#adding-new-products-later)
- [Managing your listings](#managing-your-listings)
- [Changing a category](#changing-a-category)
- [Filters](#filters)
- [When something is denied](#when-something-is-denied)
- [Moving a product to another marketplace](#moving-a-product-to-another-marketplace)
- [Tags: the complete rules](#tags-the-complete-rules)
- [Pausing or closing your connection](#pausing-or-closing-your-connection)
- [Limits and rules](#limits-and-rules)
- [Need help?](#need-help)

## What is Shop Import?

Shop Import connects your WooCommerce store to Oglasino. Here is the whole idea in four sentences:

1. In your shop, you put a **tag** (a small label) on every product you want on Oglasino.
2. Oglasino reads those products from your shop and creates listings from them.
3. From then on, Oglasino checks your shop regularly. If you change a price or a photo, or a product sells out, the listing updates by itself.
4. You never have to enter products by hand again.

Two important things to know before you start:

- **Oglasino can only read your store. It can never change it.** You will create a special "Read only" key for us. Nothing we do can touch your shop.
- **Nothing appears on Oglasino without your permission.** New products go through a short review by our team first, and even after approval, *you* decide when they go live. There are no surprises.

## Before you start

You need:

- A WooCommerce (WordPress) store that is online.
- The admin login for that store (you must be able to open its Dashboard).
- About 15–20 minutes.
- A rough idea of which products you want on Oglasino — all of them, or just some.

That's it. Ready? Let's go.

## Quick start

The whole process, in one list. Every step is explained in detail further down.

1. In WooCommerce, create a tag (for example `oglasino`).
2. Put that tag on every product you want on Oglasino.
3. In WooCommerce, create an API key with **Read** permission. Copy both keys it gives you.
4. On Oglasino, open your dashboard and go to **Shop**. Choose **WooCommerce**.
5. Enter your store address and paste the two keys.
6. Choose which marketplace your products go to, and enter your tag.
7. Match your shop's categories to Oglasino's categories, and set the filters.
8. Press **Submit for review** and wait — our team checks everything.
9. When the review is done, you get a notification. Go to **Ready For Sync** and publish your approved products.

Done. From that moment your shop and Oglasino stay in sync automatically.

## Step 1: Prepare your WooCommerce store

Everything in this step happens in your **WooCommerce admin page** — not on Oglasino.

### Create the tag

A tag is just a label. It's how you tell Oglasino "I want *this* product on Oglasino" — only tagged products are imported. Everything else in your shop is ignored.

1. In your WordPress admin menu, go to **Products → Tags**.
2. In the **Name** field, type the tag you will use for Oglasino. `oglasino` is a good, simple choice — but the name is up to you. Remember it, you'll need it later.
3. Click **Add new tag**.
4. Your new tag appears in the list on the right.

![Creating the tag in WooCommerce](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/woo-product-tags-page.png)

### Put the tag on your products

Now mark the products you want on Oglasino. The fastest way is to tag many products at once:

1. Go to **Products → All Products**.
2. Tick the checkbox next to every product you want on Oglasino. (You can tick the box at the very top to select the whole page.)
3. In the **Bulk edit** dropdown above the list, choose **Edit**, then press **Apply**.

![Selecting products for bulk tagging](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/woo-bulk-tag-select.png)

4. A panel opens above the products. Find the **Tags** field, type your tag (`oglasino`), and press **Update**.

![Typing the tag in the bulk edit panel](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/woo-bulk-tag-apply.png)

That's it — those products are now marked for Oglasino.

To tag a single product (for example a new one you add next month): open the product for editing, find the **Product tags** box on the right side, type your tag, and update the product.

![Tagging one product](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/woo-product-tag-single.png)

### Create the API key

An API key is like a special password. It lets Oglasino *read* the products from your store. You will create it with **Read** permission only — that means Oglasino can look, but can never change or delete anything in your shop.

The key comes in two parts: a **Consumer key** and a **Consumer secret**. You will copy both and paste them into Oglasino in Step 2.

1. In your WordPress admin menu, go to **WooCommerce → Settings**.
2. Open the **Advanced** tab.
3. Click **REST API keys**.
4. Click **Add key**.

![Where to create the API key](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/woo-rest-api-page.png)

5. Fill in the form:
   - **Description:** type `Oglasino` (so you remember what this key is for).
   - **User:** choose your own admin account.
   - **Permissions:** choose **Read**. Not "Read/Write" — just **Read**. This is what guarantees Oglasino can never change your store.
6. Click **Generate API key**.

![Filling in the key form](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/woo-api-key-form.png)

7. The next page shows your two keys: the **Consumer key** (starts with `ck_`) and the **Consumer secret** (starts with `cs_`). **Copy both of them now** — paste them somewhere safe, like a note on your computer.

**Important:** WooCommerce shows the secret key **only this once**. If you leave the page without copying it, you can't get it back — you'd have to delete the key and make a new one. Not a disaster, but annoying. So: copy both, right away.

![Copy both keys immediately](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/woo-api-key-generated.png)

Your store is ready. Now over to Oglasino.

## Step 2: Connect your store on Oglasino

Log in to Oglasino and open your dashboard. In the menu you'll find a **Shop** section — that's home base for everything in this guide. Inside it: **Connection**, **Shop Products**, **New products**, **Ready For Sync**, **Category mappings** and **Issues**. Don't worry about what they all mean yet — the guide covers each one.

Open **Connection**. A short wizard starts. You can stop and come back any time; nothing is final until you press **Submit for review** at the end. If you want to start over, press **Discard draft** — your store credentials are never saved from a discarded draft.

### Choose a platform

Pick **WooCommerce**.

![Choosing WooCommerce](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-shop-platform.png)

### Connect your store

Three fields:

- **Store URL** — your shop's address, starting with `https://`. For example `https://yourshop.com`.
- **Consumer key** — paste the `ck_...` key you copied in Step 1.
- **Consumer secret** — paste the `cs_...` key.

The key fields hide what you type, like password fields. Press the eye icon (**Show value**) if you want to check what you pasted.

Below the fields, this step also holds your connection's switches. You can change all of them later, so don't agonize here:

- **Auto-activate imported products** — On: products become visible as soon as they're imported. Off: they keep syncing, but stay hidden until you activate them yourself. (Not the same as Pause — Pause stops syncing completely.)
- **Auto-release after the first review** and **Auto-release after later reviews** — whether approved products go live by themselves after a review, or wait for you. Explained properly in [Step 4](#step-4-publish-your-products).
- **Sync interval (minutes)** — how often we check your shop for changes. Starts at 360 (every 6 hours); the minimum is 60.

![Entering your store address and keys](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-wizard-credentials.png)

When you continue, Oglasino connects to your store and checks everything — you'll see "Validating your store…". If something is wrong, you get a clear message. The two most common ones:

- *"The store rejected your API keys."* — Check that you pasted both keys completely, and that the key has **Read** permission.
- *"We can't reach your store."* — Check the address, and that your site is actually online.

### Sites & tags

Oglasino runs more than one marketplace — the general marketplace and the moto marketplace. On this step you choose **where your products go**, and **which tag** marks them.

1. Tick the marketplace (or marketplaces) you want to publish to.
2. For each one, enter the tag you created in Step 1 into the **Product tags** field.

The rule is simple: only products carrying one of these tags are imported, and **one product can belong to only one marketplace**. If you sell on both marketplaces, use a different tag for each (for example `oglasino` for one, `oglasino-moto` for the other) — and give each product only one of them.

You can enter several tags for one marketplace, separated by commas. Any of them counts.

![Choosing the marketplace and entering your tag](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-wizard-sites-tags.png)

### Category mapping

Now Oglasino reads your tagged products and groups them by *your* shop's categories. For each of your categories, you say which **Oglasino category** those products belong to. That's called a mapping. Example: your category "Winter socks" → Oglasino's category "Socks".

To make it faster, Oglasino suggests the closest match for each of your categories — you'll see a **Suggested** label. You can accept the suggestion, change it, or leave a category unmapped (unmapped just means those products won't get a category from the mapping — you'd set them one by one).

- The category you pick for a section applies to **every product in that section**...
- ...unless you open a product and give it its **own** category. A product's own pick always wins.

**Not sure which category fits?** Pick your best guess and move on. Our team checks every product during the review and corrects categories where needed. You cannot get this "wrong" in any harmful way.

Every product needs a category before you can submit — the wizard shows you a count of products still missing one.

![Matching your categories to Oglasino's](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-wizard-mapping.png)

### Filters

Filters are the small details buyers use to narrow their search — things like condition (new or used) and delivery. Listings with good filters are found more often, so this step is worth a minute.

You set filter values **once per section**, and every product in that section uses them. Just like categories, a single product can have its own values instead — open the product, press **Edit filters**, and change what you need. A value you set on a product yourself shows an **Overridden** badge, and you can always go back with **Reset to section**.

Two special things:

- A filter marked **Required** must have a value before you can submit. (In the beginning that's *condition* — new or used.)
- The *availability* filter is handled automatically from your shop's stock. You never set it.

![Setting section filters](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-wizard-filters.png)

![The product filter dialog](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-wizard-product-filters.png)

### Review and submit

The last step shows a summary of everything: your store, the marketplace, the tag, how many products, the categories. One more thing to know, in plain words:

> After you submit, your products go to our team for review. Nothing appears on the site until it's approved.

Also good to know: your product photos come straight from your shop, and they will be displayed on Oglasino.

Happy with the summary? Press **Submit for review**.

![The final summary](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-wizard-review.png)

## Step 3: The review

After you submit, your connection shows **Awaiting review**. Here is what that means, honestly and completely:

- Our team looks at every product you sent — names, photos, categories — and approves each one, or refuses it with a short explanation. If you picked a wrong category somewhere, we simply correct it.
- **While the review is open, that batch is locked.** You can't edit those products, and you can't see the decisions as they happen. This is on purpose: all decisions arrive **at once**, when the review is finished, so you get one clear result instead of a confusing trickle.
- Your shop keeps working normally the whole time, of course — the review only concerns what's on Oglasino.

When the review is done, you get a notification (in the app and by email). Then:

- **Approved products** are ready to publish — see the next step.
- **Refused products** (if any) appear on your **Issues** page, each with the reason. You can fix things or ask for another review — see [When something is denied](#when-something-is-denied).

![While your review is running](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-pending-review.png)

## Step 4: Publish your products

Here's a rule Oglasino never breaks: **a listing never goes live without your say-so.** Approval by our team is not publishing — *you* publish (or you flip a switch that publishes for you; both are your call).

Open **Ready For Sync**. Every approved, not-yet-published product waits here.

- Publish one product, tick several and press **Release selected**, or press **Release all**.
- A released product becomes a live listing on the marketplace, visible to buyers.
- Occasionally a row is disabled with a note — that product is waiting on something (for example a category change that's still in review). Only that row is blocked; everything else can go.

![Publishing from Ready For Sync](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-ready-for-sync.png)

**Don't want to click every time?** Two of the switches from Step 2 handle it:

- **Auto-release after the first review** — when your first review finishes, approved products go live right away.
- **Auto-release after later reviews** — same, for every review after the first.

With both off, everything always waits for you on Ready For Sync. And the third switch, **Auto-activate imported products**, decides how products arrive: On, they become visible as soon as they're imported; Off, they keep syncing but stay hidden until you activate them yourself.

All three are your choice, and you can change them any time on your **Connection** page.

![Your connection's switches](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-connection-settings.png)

## How syncing works

Once your first review is finished, your connection becomes **Active** and Oglasino starts checking your shop regularly. "Sync" just means that check.

**What updates automatically on your live listings:**

- Price changes.
- Name, description and photo changes.
- Stock: a product that sells out is taken offline automatically; when it's back in stock, it comes back online. (This never overrides your own choices — a product you hid stays hidden.)
- New tagged products are *discovered* — they appear on your **New products** page, waiting for you. See [Adding new products later](#adding-new-products-later).

**What NEVER happens automatically:**

- Publishing a new listing. New products always go through review, and then through Ready For Sync (or your auto-release switch). Always.

**Timing and control:**

- How often we check is the **Sync interval** on your Connection page. The default is every 6 hours; the minimum is 60 minutes.
- Impatient? Press **Sync now** on the Connection page for an immediate check. (Once per hour.)
- The Connection page always shows your **Last sync**: when it ran, what it did (created / updated / removed counts), and any products it skipped, with the reason.

If a sync skips a product, the reason tells you whose move it is: something to fix in your store, a temporary problem that retries by itself, or something on our side where you don't need to do anything.

## Adding new products later

This is the everyday routine, and it's short:

1. In WooCommerce, put your tag on the new product. That's the only thing you do in your shop.
2. On the next sync, the product appears on your **New products** page on Oglasino.
3. It usually already has a category (from your mapping). Change it if you like, or pick one if it's missing — a product can't be sent without a category.
4. Set its filters if needed (required filters must have a value).
5. Tick the products and press **Send selected**.
6. The batch goes to review. When it's done, you get a notification, and approved products land on **Ready For Sync** as usual.

Products that can't be sent yet are highlighted with the reason right on the row — most often "pick a category first" or a tag problem (see [Tags: the complete rules](#tags-the-complete-rules)).

![New products waiting for you](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-new-products.png)

## Managing your listings

**Shop Products** lists every live listing that came from your shop. Open any product there to see its actions: preview the listing, view it in your shop, request a category change, or edit its filters.

![A product's actions](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-product-actions.png)

From this page you can:

- Open any listing to see it as buyers see it.
- **Hide a listing.** Hiding takes it offline for buyers, but it keeps receiving updates from your shop the whole time (price, stock, photos). When you want it back, press **Unhide** — the next sync brings it back online. Hiding is per-listing and completely reversible.
- **Request a category change** for a product — see the next section.

Good to know: listings imported from your shop are *managed by your shop*. You edit the product in WooCommerce — not on Oglasino — and the changes flow in on the next sync. That's the whole point: one place to edit.

![Your live shop listings](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-shop-products.png)

## Changing a category

Categories are the one thing that goes through review even after a product is live — a category decides where buyers find your product, so our team confirms changes. Two kinds:

**Change one product's category.** On **Shop Products**, open the product and press **Request category change**. Pick the **New category**, set the filters for it, and choose what happens while the request waits:

- **Hide until decided** — the listing goes offline until the review is done.
- **Leave active** — the listing stays live under its current category until the review is done.

Then **Send change request**. If it's approved, the change applies automatically and the product goes (or stays) live. If it's refused, everything stays exactly as it was, and you'll find the reason on **Issues**. While the request waits, that product shows **In review** and its change button is disabled — one open request at a time.

**Change a mapping's default category.** The **Category mappings** page lists each of your shop categories and its default Oglasino category — the one future products inherit.

- A row without a default has **Set default category**. A first default affects future products only — and it goes through a quick review.
- A row with a default has **Change default category**. When the change is approved, products already using that default are updated to the new category too. Products you gave their own category are never touched.
- A default our team has confirmed shows a **Confirmed** badge.

While a review involving a mapping is open, its buttons are disabled with a short explanation — never gone, just waiting.

![Your category mappings](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-category-mappings.png)

## Filters

Everything from the wizard's filter step keeps working after launch, and you can edit filters any time — **filter edits don't go through review**.

- **Section filters:** on **Category mappings**, each section has a **Section filters** button. Values you save there apply to every product in the section — except products where you set your own values.
- **Product filters:** on **Shop Products** (and on **New products**), open the product and edit its filters to set values for just that product. Your own values show **Overridden**; **Reset to section** puts a value back under the section's control.
- **Required** filters must always have a value — you can change a required value, but you can't leave it empty.
- The *availability* filter is automatic (it follows your shop's stock) and can't be edited.

One honest note: because filter edits skip review, there's a daily limit on how many you can make. It's generous — you'll only ever notice it if something on your side goes haywire and fires thousands of changes.

![Editing a section's filters](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-filter-popup.png)

## When something is denied

Sometimes our team refuses a product or a category. It's not the end of anything — here's how it works.

Everything that needs your attention lives on one page: **Issues**. You'll find:

- **Denied by review** — refused products, each with the reviewer's reason. Products refused together as a group share one reason.
- **Rejected category changes** — with a **Request the change again** button if you want another try.
- **Rejected marketplace moves** — see [the moves section](#moving-a-product-to-another-marketplace).
- **Extra marketplace tags** — live products that carry a tag for another marketplace. Remove the extra tag in your shop and this clears itself. You can hide the listing meanwhile.
- **Skipped products** — products a sync couldn't import, each with the reason and whose move it is.

**Disagree with a decision?** Press **Ask for another review**. You can add a short note for the reviewer (up to 500 characters) — use it to explain what the reviewer might have missed. Your appeal goes into the normal review queue, and you'll be notified with the result. To keep the queue fair, you can appeal the same thing again only after a few days.

If a whole *category* of yours was refused, its products are taken off the marketplace together, and they come back together if the decision is reversed — you don't have to do anything per product.

![The Issues page](https://raw.githubusercontent.com/memento-tech/oglasino-platform/refs/heads/main/assets/en/app-issues.png)

## Moving a product to another marketplace

Sold something on the general marketplace that really belongs on the moto marketplace (or the other way around)? Just change its tag in your shop:

1. In WooCommerce, remove the old marketplace's tag and add the other marketplace's tag.
2. On the next sync, the product shows up under **Marketplace moves** on your **Issues** page.
3. Pick a category for it **on the new marketplace** and press **Send move** — a move is reviewed like a new product.
4. Your live listing **stays live** on the old marketplace the whole time. Nothing disappears while you wait.
5. When the move is approved, you publish it like any approved product (Ready For Sync or auto-release). The listing moves — with its reviews, favorites and messages intact.

One thing changes: the listing's web address, because it now lives on another marketplace. Old links to it will stop working. If you don't want the move after all, put the old tag back — done.

## Tags: the complete rules

The tag is your steering wheel. Here is everything a tag change does, in one table:

| You do this in your shop | What happens on Oglasino |
| --- | --- |
| Add your tag to a product | It appears on **New products**, waiting for you to send it to review |
| Remove the tag from a live product | The listing goes offline immediately. Nothing is deleted — it's your product, your call |
| Put the tag back | The listing comes back online on the next sync |
| Swap between two of your tags for the *same* marketplace | Nothing changes |
| A product carries several tags for the same marketplace | Fine — any one of them counts |
| Change the tag to the *other* marketplace's tag | The product goes through the move flow ([see above](#moving-a-product-to-another-marketplace)) |
| Add an *extra* tag for the other marketplace to a live product | The listing stays where it is and keeps updating, but you get an entry on **Issues** — remove the extra tag to clear it |
| Give a *new* product tags for both marketplaces | It waits on **New products** marked "fix the tag" — it can't be sent until only one marketplace remains |
| Delete a product in WooCommerce entirely | Its Oglasino listing is removed too. If you re-create it in your shop later, it starts over as a new product |

## Pausing or closing your connection

**Pause** (on the Connection page) stops syncing entirely — nothing updates, nothing is discovered — until you press **Resume**. Your listings stay as they are. Use it for holidays or shop maintenance.

If your store credentials stop working (for example the key was deleted in WooCommerce), the connection pauses itself and tells you — re-enter the keys and re-validate to resume.

**Close connection** ends the whole thing. Because your listings matter, closing always asks what should happen to them — you choose one of three:

- **Keep my listings** — they stay on Oglasino and become normal listings you edit yourself, no longer tied to your shop.
- **Deactivate my listings** — they're hidden and unlinked; you can reactivate and edit them later.
- **Delete my listings** — they're removed from Oglasino and their photos are deleted.

Closing is confirmed by typing **CLOSE** — it's not something to do by accident.

## Limits and rules

Everything in one place, no surprises:

- **API key permission:** always **Read**. Oglasino never writes to your store.
- **Store address:** must start with `https://`.
- **One marketplace per product.** A product's tags decide its marketplace, and it can have only one.
- **Sync interval:** minimum 60 minutes; default every 6 hours.
- **Sync now:** once per hour.
- **Retrying skipped products:** up to 10 products per hour.
- **Product limit:** normally there is none. Oglasino can set a cap on how many products a connection may import; if a cap applies to you, it's shown on your Connection page, and products over it appear under Skipped products.
- **Appeal note:** up to 500 characters (and it's optional).
- **Names and descriptions:** very long ones are shortened automatically to fit Oglasino's listing format — names to 80 characters, descriptions to 2000.
- **Filter edits:** no review, but a generous daily limit applies.
- **Store currency:** your shop's currency must be one the marketplace supports — you'll be told at connection time if it isn't.

## Need help?

Write to **support@oglasino.com** — tell us your store address and what you were trying to do, and we'll sort it out with you.
