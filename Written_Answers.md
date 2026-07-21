# Written Answers - Question 2 & Question 3

The two questions below are qualitative, so there's no code to run for them.
Question 1's full working (merges, aggregations, charts) is in
`Sales_Analysis.ipynb` - these are just the write-ups for the parts of the
assignment that ask for opinion and product thinking rather than analysis.

---

## Question 2: App Exploration

I spent time going through the Jar app on a personal account before writing
this - the save flows, the redemption side, the referral/gamification bits,
and the settings/KYC screens. Below are the five things that stood out as
genuinely well done, and five places where I'd push back or improve things,
with the reasoning behind each.

### Five things that work well

1. **Round-off saving removes the "decision" from saving.** Instead of
   asking the user to remember to save, it hooks into UPI transactions and
   invests the spare change automatically. The whole reason most people
   don't save small amounts consistently is that it requires a repeated,
   conscious decision - Jar just deletes that step. This is the single
   feature that made the app feel different from a regular gold-buying app
   rather than a "nice-to-have" add-on.

2. **₹10 minimum ticket size actually lowers the psychological barrier, not
   just the financial one.** A lot of savings products advertise "start
   small" but still make ₹500 feel like the real entry point. Being able to
   buy in single-digit rupee amounts means a first-time user can try the
   product without it feeling like a financial commitment, which matters a
   lot for people who've never invested in anything before.

3. **The streak/gamification layer gives saving a feedback loop.** Daily
   save streaks, small visual rewards, and progress indicators borrow
   directly from habit-forming app design (the kind you'd see in a
   language-learning app), and it works because saving money otherwise has
   almost no immediate feedback - you don't "feel" ₹20 going into gold the
   way you feel a streak counter going up.

4. **Redemption flexibility is more thought-through than I expected.** Being
   able to cash out, or alternatively convert savings into actual gold
   coins/jewellery through partner jewellers, means the product doesn't
   force a single exit path. For a user who started saving without a clear
   goal in mind, having options at the end rather than only at the start is
   a good design call.

5. **Trust signals around the gold itself are handled well.** 24K
   certified gold, clear custody/storage messaging, and transparent
   real-time pricing address the most obvious objection a first-time user
   would have ("is this actually backed by real gold, or is it just a
   number in an app?"). Getting this reassurance in early, rather than
   burying it in T&Cs, is probably doing a lot of quiet work on conversion.

### Five areas I'd improve

1. **The connection between "saving" and "investing" isn't explained
   clearly enough inside the flow itself.** A first-time user rounding off
   their chai payment may not fully register that they're buying a
   commodity whose price moves daily, gold. A short, one-time explainer
   woven into the round-off setup (not a separate help article) would set
   expectations better and reduce confusion later when the redemption value
   isn't exactly what they'd expect.

2. **There's no visible way to compare gold savings against a benchmark or
   alternative.** Someone using the app for months has no easy way to see
   "here's what this would look like against a recurring deposit" or
   similar. Even a simple, non-prescriptive comparison view (not advice,
   just information) would help retention for users deciding whether to
   keep going or move the money elsewhere.

3. **Goal-based saving feels bolted on rather than central.** The core loop
   is very good at "save a little, automatically", but less good at helping
   someone plan toward a specific outcome (a wedding, a gift, a specific
   gram target) with a visible countdown or milestone structure. Given how
   much of the emotional appeal of gold-buying in India is tied to specific
   occasions, this feels like an underused hook.

4. **Notifications lean more toward re-engagement nudges than genuinely
   useful updates.** A user checking in after a price swing or a milestone
   in their own savings is a much stronger moment to message them than a
   generic "come back and save today" push. The current mix felt weighted
   toward the latter.

5. **The onboarding/KYC step, while necessary, is where a chunk of curious
   first-time users will likely drop off**, since it's a harder ask than
   the ₹10 entry price suggests. Letting a user save a very small amount in
   an unverified "preview" state before asking for full KYC (converting to
   real gold only after verification) could let people experience the
   product before being asked to commit personal documents - right now
   those two asks happen almost back-to-back.

---

## Question 3: Product Exploration - New Business Opportunities

Jar's actual asset isn't gold - it's the habit it's built and the trust
that comes with being the thing people let auto-debit their account every
day. Digital gold was the right first product to earn that trust because
it's simple to understand, low-risk in the way most Indian households
already think about gold, and works at a ticket size nothing else in
fintech was offering. But the same rails - automation, tiny ticket sizes,
and a user base that already trusts Jar with recurring small debits - can
carry more than one product. A few directions I think make sense, roughly
in order of how close they are to what Jar already does:

**1. Broader micro-investing beyond gold.** The obvious next step is
extending the same round-off/auto-save mechanism to other asset classes -
short-duration debt funds, index funds, or even fractional silver - for
users who've built a saving habit and are ready to diversify. The point
isn't to compete head-on with mutual fund apps on features; it's to let the
existing round-off engine feed into more than one destination, with gold as
the default and other options as an upgrade path for users who stick
around. This keeps the automation-first identity intact while raising the
ceiling on what a long-term user can do with the app.

**2. Gold-backed credit.** Once a user has an accumulated gold balance
sitting with Jar, offering a small, instant loan against that balance (or a
gold-backed credit line) is a natural extension - the collateral already
exists, the user is already KYC'd, and it solves a real short-term liquidity
need without asking the user to sell an asset they've been deliberately
building. This is a genuinely differentiated offering, since most lenders
can't underwrite this cheaply or this fast because they don't already hold
the collateral.

**3. Insurance and protection products, sold in the same small-ticket
language.** Micro-insurance (accident cover, small health top-ups) framed
the same way as the savings product - "₹10 a day" rather than "an annual
premium" - would fit the same psychological model that made gold savings
work. Jar wouldn't need to be the insurer; a distribution tie-up with an
existing insurer, wrapped in Jar's UX and auto-debit rails, is enough to
test demand cheaply.

**4. A family/group savings layer built around real-life goals.** Buddy
savings already exists in a basic form; extending it toward specific
occasions - a family wedding fund, a child's education fund, a group gift -
with visible milestones and light social pressure (in a positive sense: a
shared goal others can see progress on) plays directly to how gold-buying
already works culturally in India, and gives the app a reason to be opened
for something other than "did my auto-save go through today."

**5. Data-backed credit scoring as a longer-term moat.** This one's more
speculative, but a user with a year or more of consistent, automated saving
behavior is showing something a bureau score doesn't capture - discipline
and consistency, even at small amounts. Over time, that saving history
could become a legitimate underwriting signal Jar could use itself (for
point 2 above) or potentially offer as an alternative-data input to
partner lenders, for users who are otherwise thin-file or new-to-credit.
This is the kind of thing that takes years of consistent data to be
trustworthy, so it's worth starting to think about even though it isn't a
near-term launch.

The common thread across all of these is that none of them ask Jar to
abandon what it's good at - small ticket sizes, automation that requires no
ongoing decision from the user, and a lot of accumulated trust from a
product that's already proven itself with real money. The risk to avoid is
trying to become a full-blown financial supermarket too quickly and diluting
the one thing that made the first product work: it did one small thing
extremely well before asking for anything else.
