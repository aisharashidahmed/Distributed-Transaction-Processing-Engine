# 1. Who Is This Platform For?

**Purpose**

Define the platform's target users, accessibility goals, and overall product positioning.

---

### 1.1 Are you targeting first-time retail investors, or people who already invest and want a better experience?

**Answer**

The platform is designed for both first-time retail investors who are beginning their investing journey and existing investors who want a better, more transparent, and user-friendly investment experience.

**Reason**

Building for both audiences aligns with the platform's mission of making investing accessible while still providing a high-quality experience for users who already invest.

**Validation Question**

> What needs or pain points do experienced investors have today that are not being solved by existing investment platforms?

---

### 1.2 Are you building for urban, mobile-money-savvy users, or trying to reach underserved/rural populations too?

**Answer**

The initial target audience is urban, mobile-money-savvy Kenyans.

The platform should be designed with a simple, intuitive user experience so it can naturally expand to underserved and rural populations in the future.

**Reason**

Urban users are more likely to have smartphones, reliable internet access, and familiarity with digital financial services such as M-Pesa, making them the most practical audience for an initial launch.

**Validation Question**

> What barriers currently prevent underserved and rural populations from investing, beyond simply having access to a mobile application?

---

### 1.3 Diaspora Kenyans investing back home — in scope or not?

**Answer**

Yes. Diaspora Kenyans are part of the platform's long-term target audience.

The initial launch will focus on users residing in Kenya. Support for diaspora investors will be introduced in a later phase due to additional identity verification, payment, foreign exchange, taxation, and regulatory considerations.

**Reason**

Many Kenyans living abroad want to build wealth and invest back home. Supporting them aligns with the platform's long-term vision of making Kenyan investments more accessible.

**Validation Question**

> What additional regulatory, identity verification, payment, and tax requirements apply when serving diaspora investors?

---

### 1.4 What's the minimum amount someone should be able to invest?

**Answer**

The platform will not impose a universal minimum investment amount.

Instead, each investment product will have:

* a recommended starting amount,
* any provider or issuer minimum,
* and any market or broker minimum.

#### Initial Recommended Starting Amounts

* **Money Market Funds:** KSh 100
* **Stocks:** KSh 500
* **REITs:** KSh 500
* **Government Bonds:** Product-specific

**Reason**

Different investment products have different structures and constraints. Recommendations help guide new investors without creating unnecessary barriers.

**Validation Question**

> Across each supported investment category, what market, provider, fee, and operational constraints determine the smallest practical investment amount?

---

# 2. What Can People Actually Invest In?

**Purpose**

Define the investment products the platform will support and how users access them.

---

### 2.1 NSE-listed equities only, or also government bonds/T-bills, unit trusts/money market funds, REITs?

**Answer**

Version 1 will support:

* NSE-listed equities
* Money Market Funds
* Government Bonds and Treasury Bills
* REITs

The platform will not initially support:

* Crypto
* Forex
* CFDs
* Options
* Futures
* Commodities

**Reason**

The platform prioritizes long-term wealth-building through ownership and income-generating investments before expanding into speculative or derivative products.

**Validation Question**

> What regulatory, licensing, and operational requirements are needed to offer all four investment categories through a single platform?

---

### 2.2 Will you support fractional shares, or only whole shares?

**Answer**

Version 1 will support whole-share investing for NSE-listed equities.

The platform architecture should remain capable of supporting fractional investing in the future if permitted by the broker, custodian, exchange, and regulatory framework.

**Reason**

Current Kenyan market infrastructure supports trading in single whole shares. Fractional ownership depends on custody and market infrastructure, not just application design.

**Validation Question**

> If a technology platform wanted to offer fractional ownership of NSE-listed equities, what legal, operational, and custody model would make that possible?

---

### 2.3 Single asset class at launch, with others added later, or multi-asset from day one?

**Answer**

The platform will launch as a multi-asset investment platform supporting Stocks, Money Market Funds, Government Bonds, and REITs.

Not every investment category must have full transaction capabilities on day one, but they will all be represented within the platform from Version 1.

**Reason**

The platform exists to help Kenyans invest, not simply trade stocks. Different investment products serve different financial goals, risk profiles, and life stages.

**Validation Question**

> If a technology platform wanted to offer Stocks, MMFs, Government Bonds, and REITs through one user experience, what regulatory, operational, or licensing considerations would determine whether they can all be offered under one platform?

---

# 3. Regulatory & Custody

**Purpose**

Define how the platform interacts with Kenya's regulated financial infrastructure while maintaining a simple and trustworthy user experience.

---

### 3.1 Since there's no central retail investing platform, will you be a licensed investment/fund manager yourself, or a technology layer sitting on top of licensed brokers/CDSC?

**Answer**

Version 1 will operate as a technology platform that partners with licensed financial institutions rather than becoming a licensed intermediary itself.

The platform will focus on customer experience, investment education, onboarding, portfolio management, investment discovery, and integration with licensed financial institutions. Regulated partners will continue performing activities that legally require licences, such as brokerage, custody, and trade execution.

**Reason**

Launching as a technology platform allows the company to focus on solving accessibility and user experience while leveraging existing regulated financial infrastructure. This reduces regulatory complexity, operational risk, and time to market, while leaving open the possibility of bringing more regulated functions in-house in the future if it becomes strategically beneficial.

**Validation Question**

> What is the most appropriate regulatory and licensing structure for a technology platform that provides a unified investment experience while partnering with licensed brokers, custodians, and investment managers?

---

### 3.2 Who actually holds custody of client funds and securities — you, a partner broker, or a custodian bank?

**Answer**

Client funds and investment assets will initially be held by licensed partner institutions rather than by the platform itself.

The platform will provide the user experience through which customers manage their investments, while regulated partners remain responsible for custody.

**Reason**

Separating custody from the technology platform increases customer protection, leverages existing regulated institutions, reduces operational and regulatory risk, and ensures that customer assets remain protected even if the platform itself experiences operational issues.

**Validation Question**

> What custody model best protects customers while allowing a technology platform to provide a unified investment experience?

---

### 3.3 What CMA license category do you need?

**Answer**

The platform will be designed around its intended operating model rather than around a predetermined licence category.

The appropriate CMA licensing structure will be determined based on the final business model in consultation with the CMA and legal counsel.

**Reason**

Licences regulate activities, not ideas. The company should first define exactly what services it performs and which regulated activities remain with licensed partners before determining the appropriate licensing structure.

**Validation Question**

> Given this operating model, what is the most appropriate CMA licensing structure, and are there any additional approvals or registrations required?

---

### 3.4 Do you need a CDS (Central Depository System) account setup per user, and how will that onboarding work?

**Answer**

If a CDS account is required for a user's investments, The platform will provide a seamless onboarding experience for any required CDS account creation through its licensed partners.

Users should feel like they are creating an investing account while still having full visibility into their CDS account details and official investment records within the platform.

**Reason**

The platform should abstract unnecessary complexity while remaining completely transparent. Users should not have to understand financial infrastructure before they can begin investing, but they should always be able to access and view their official CDS account information whenever they choose.

**Validation Question**

> Can a technology platform initiate and manage the CDS account opening process on behalf of users, and what legal, operational, and technical requirements would that involve?

---

### 3.5 KYC/AML requirements — what identity verification is mandatory before someone can invest?

**Answer**

The platform will adopt a **browse first, verify before investing** approach.

Users will be able to explore investment products, learn about investing, compare opportunities, and use educational features without completing identity verification.

However, full KYC verification will be required before a user can:

* Deposit funds
* Purchase investments
* Withdraw funds

As the platform grows, more advanced fraud detection, risk monitoring, and identity verification measures will be introduced to strengthen security while maintaining a smooth user experience.

**Reason**

This approach minimizes unnecessary onboarding friction while ensuring all regulated financial activities comply with KYC and AML requirements. It allows users to understand the platform before providing sensitive personal information while still protecting the integrity of the financial system.

**Validation Question**

> What are the minimum KYC and AML requirements that must be completed before a user is legally permitted to fund an account and make their first investment?

# 4. Money Movement

**Purpose**

Define how users move money into and out of the platform while ensuring transparency, trust, and a seamless investment experience.

---

### 4.1 How does money get in and out?

**Answer**

Version 1 will launch with **M-Pesa as the primary payment rail**, while the payment architecture remains provider-agnostic.

The platform will be designed so additional payment methods (such as Airtel Money, bank transfers, debit cards, and future payment providers) can be integrated without redesigning the platform.

**Reason**

M-Pesa provides the most familiar and accessible payment experience for the platform's initial target audience. However, the platform should remain independent of any single payment provider and support multiple payment rails as it grows.

**Validation Question**

> What payment architecture would allow the platform to integrate multiple payment providers (e.g., M-Pesa, Airtel Money, banks) while maintaining a consistent user experience and complying with financial regulations?

---

### 4.2 Instant top-ups vs. settlement delays for actual trade execution — how will you handle that gap in the UX?

**Answer**

The platform will always reflect the true state of every transaction while presenting it in a way that is intuitive and reassuring for users.

Users should immediately receive confirmation when an order has been successfully placed or executed, while the platform clearly communicates when settlement is still in progress. The interface should celebrate successful actions without misrepresenting ownership or the completion of underlying financial processes.

**Reason**

Financial infrastructure naturally introduces delays between deposits, order execution, settlement, and withdrawals. The platform should never hide or misrepresent these states, but it should also avoid making normal financial processes feel like errors or unnecessary complexity.

The user experience should balance transparency with confidence by clearly communicating what has happened, what is happening, and what happens next.

**Validation Question**

> What transaction states should be exposed to users, and at what point in the investment lifecycle should each state transition be displayed to remain both accurate and intuitive?

---

### 4.3 Withdrawal speed and limits — what's realistic given your custody/broker setup?

**Answer**

The platform will communicate withdrawal status transparently and reflect the timelines of the underlying custody, settlement, and payment infrastructure.

Where possible, withdrawals should be processed as quickly as the financial ecosystem allows, but the platform will prioritize accurate status updates and clear expected completion times over promising unrealistic speeds.

**Reason**

Withdrawal speed depends on external factors including settlement, custody, payment providers, and regulatory processes. The platform should not create expectations it cannot consistently meet. Instead, users should always understand where their withdrawal is, why it may take time, and when they can realistically expect to receive their funds.

**Validation Question**

> Given the proposed custody and settlement model, what is the fastest realistic withdrawal experience that can be consistently delivered to customers?



# 5. Core Product Experience

**Purpose**

Define how users interact with the platform, make investment decisions, and build long-term investing habits while maintaining a simple, trustworthy, and intuitive user experience.

---

### 5.1 Real-time or delayed market data?

**Answer**

Version 1 will display delayed market data, with prices delayed by approximately 15 minutes.

The platform will clearly communicate when prices were last updated and when the next update is expected.

Each investment page should display:

* Current Price
* Last Updated
* Next Update
* Historical Price Chart

Users will still be able to place both Market Orders and Limit Orders.

Once an order has been executed, users will receive a notification and their portfolio will update to reflect the completed transaction.

Real-time market data may be introduced in a future version of the platform.

**Reason**

Delayed market data reduces licensing costs and implementation complexity while remaining sufficient for the platform's primary audience of long-term investors. Clearly communicating the age of market data maintains transparency and user trust without requiring expensive real-time infrastructure during the initial launch.

**Validation Question**

> What licensing, technical, and commercial requirements apply to offering real-time NSE market data, and when would introducing it become commercially justifiable?

---

### 5.2 Self-directed investing (user picks investments) vs. guided investing (goal-based guidance)?

**Answer**

The platform will support both self-directed investing and goal-based guided investing.

Users will not be required to choose one experience permanently. Instead, both experiences will remain available throughout the platform.

Users who know what they want can immediately browse and invest in any supported investment product. Users who are unsure where to begin can use guided investing to explore investment ideas based on their financial goals.

The platform should allow users to move freely between both experiences at any time.

**Reason**

The platform should adapt to the user's needs rather than forcing them into a permanent category such as "beginner" or "experienced investor." Investing knowledge varies by investment type, financial goal, and life stage. Giving users continuous access to both guided and self-directed experiences provides flexibility while maintaining an intuitive user experience.

**Validation Question**

> At what point does goal-based guidance become regulated investment advice, and how can the platform provide educational guidance while remaining compliant with CMA requirements?

---

### 5.3 How should educational content be presented?

**Answer**

Investment education will be integrated directly into the investing experience rather than placed inside a dedicated learning section.

The platform will use progressive disclosure, presenting information based on what users need at each stage of the investment journey.

The following information should always be visible on every investment page:

* Good For
* Risk
* Investment Horizon
* Current Price
* Historical Price Chart

Concepts requiring additional explanation will be available through information (ⓘ) icons. Examples include:

* What is a Stock?
* What is a Money Market Fund (MMF)?
* What is a REIT?
* What is Investment Horizon?
* What is a Market Order?
* What is a Limit Order?
* Why is the displayed price delayed?

Users who want deeper analysis can access a dedicated **Advanced Analysis** section containing investment metrics such as Market Capitalization, P/E Ratio, Earnings Per Share (EPS), Dividend Yield, Price-to-Book Ratio, Revenue Growth, Beta, 52-week High/Low, Financial Statements, and Company Information. Each metric will include an information (ⓘ) icon explaining what it means and how it should be interpreted.

**Reason**

Users are most receptive to learning while making an investment decision rather than by visiting a separate educational section. Presenting education in context keeps the interface approachable for first-time investors while allowing experienced investors to access additional information only when they need it.

**Validation Question**

> Which educational information most effectively improves investor understanding and confidence when presented contextually throughout the investment experience?

---

### 5.4 Notifications, goal-setting, recurring and automatic investing?

**Answer**

The platform will support financial goals, recurring investing, automatic investing, and notifications that encourage long-term investing habits.

Users should be able to create financial goals and link investments to those goals.

When making an investment, users will be given the option to either:

* Invest Once
* Make this a Recurring Investment

Recurring investing should be introduced during the initial investment flow rather than requiring users to discover and configure it later.

Notifications should focus on supporting long-term investing rather than encouraging frequent trading.

Examples include:

* Goal progress updates
* Upcoming recurring investments
* Successful recurring investments
* Dividend payments
* Portfolio milestones
* Portfolio health insights
* Relevant educational content

The platform should avoid notifications designed to encourage speculative or emotional investing, such as alerts based solely on short-term market price movements.

**Reason**

The platform's objective is to help users build long-term wealth through consistent investing rather than maximizing trading activity. Goals, automation, and meaningful notifications encourage disciplined investing while reducing reliance on memory, willpower, and emotional decision-making.

**Validation Question**

> Which recurring investment defaults and notification strategies most effectively improve long-term investing consistency while maintaining user trust and minimizing notification fatigue?

# 6. Trust and Transparency

**Purpose**

Define how the platform builds and maintains user trust by making fees, investment ownership, and financial records transparent, understandable, and easily verifiable.

---

### 6.1 How will you show fees clearly (brokerage fees, CMA levies, CDSC fees, and platform fees)?

**Answer**

The platform will present a simple fee summary before users confirm an investment while providing a detailed breakdown on demand.

The investment confirmation screen will display:

* Investment Amount
* Estimated Fees & Charges
* Total You'll Pay

Users can select **Estimated Fees & Charges** to view a detailed breakdown of all applicable costs, including:

* Brokerage Fees
* CMA Levies
* CDSC or Exchange Fees (where applicable)
* Platform Fees (if applicable)
* Taxes (where applicable)

Where appropriate, users should be able to view a brief explanation of each fee through an information (ⓘ) icon.

Users should also be able to access the platform's Legal & Disclosures section from the investment confirmation flow to understand how the platform generates revenue and manages commercial relationships.

The platform will never hide fees or combine them into unexplained charges.

**Reason**

Most users want to understand the total cost of an investment without being overwhelmed by unnecessary detail. Providing a simple summary with an optional detailed breakdown balances usability with complete transparency. Clearly disclosing all fees helps build long-term trust and ensures users always understand where their money is going.

**Validation Question**

> What fees are legally required to be disclosed before an investment transaction in Kenya, and how should they be presented to ensure both regulatory compliance and a simple user experience?

### 6.2 What proof or statements do users receive to verify that their investments are genuinely theirs?

**Answer**

The platform will serve as the user's primary investment experience while providing access to official records that verify investment ownership.

Users should be able to view their investments, portfolio performance, and transaction history directly within the platform without needing to understand the underlying custody infrastructure.

For every investment, the platform will make official ownership records easily accessible, including:

* Trade Confirmations
* Broker Contract Notes
* CDS Statements (where applicable)
* Tax Documents (where applicable)

The platform will also generate its own user-friendly investment statements, including monthly portfolio statements summarizing:

* Portfolio Value
* Investment Holdings
* Contributions
* Investment Returns
* Dividends Received
* Transaction History

Platform-generated statements are intended to help users understand and monitor their investments, while official documents remain the legal record of ownership.

**Reason**

Users should not have to navigate complex financial infrastructure to feel confident that they own their investments. The platform should provide a simple and intuitive investment experience while ensuring every user has access to official documentation that verifies ownership whenever needed. Combining user-friendly portfolio statements with legally recognized ownership records strengthens transparency, confidence, and trust.

**Validation Question**

> What official ownership documents are generated by brokers, custodians, CDSC, and other investment providers, and how can a technology platform securely present those documents alongside its own portfolio statements while allowing users to independently verify ownership?

### 6.3 How will the platform manage conflicts of interest arising from commercial partnerships?

**Answer**

The platform will prioritize the interests of users when presenting investment opportunities.

Commercial partnerships, revenue-sharing agreements, or other business relationships will not determine how investments are ranked, recommended, or presented to users.

Investment discovery and recommendations should be based on objective, user-focused criteria such as investment characteristics, financial goals, risk profile, and user preferences.

Where promotional content or sponsored investment opportunities are presented, they must be clearly identified as sponsored.

The platform will publicly disclose how it generates revenue and maintain a dedicated Legal & Disclosures section explaining commercial partnerships and potential conflicts of interest.

**Reason**

Trust is fundamental to long-term investing. Users should have confidence that investment recommendations are designed to support their financial goals rather than maximize platform revenue. Clearly separating commercial relationships from investment recommendations strengthens transparency, credibility, and long-term user trust.

**Validation Question**

> What disclosure requirements and best practices apply to commercial partnerships, sponsored financial products, and conflicts of interest for investment platforms operating in Kenya?

# 7. Business Model

**Purpose**

Define how the platform generates sustainable revenue while aligning the interests of users, partner

### 7.1 Transaction fees, subscription, AUM-based fee, or spread on a money market product?

**Answer**

The platform will initially adopt a hybrid business model.

Revenue may come from multiple sources, including:

* Transparent platform fees where appropriate
* Commercial partnerships and revenue-sharing agreements with licensed financial institutions
* Optional premium products or features introduced as the platform matures

The platform will not rely on hidden spreads or pricing practices that obscure the true cost of investing.

As the platform delivers additional value through new products, services, and capabilities, the business model may expand while remaining transparent and aligned with user interests.
**Reason**

A hybrid business model reduces dependence on any single source of revenue while aligning the interests of users, partners, and the platform. Transparent pricing strengthens user trust, while diversified revenue streams support long-term sustainability and continued investment in improving the platform.

**Validation Question**

> Which combination of transparent platform fees, commercial partnerships, and premium services creates a sustainable business model while remaining competitive and aligned with the platform's mission of making investing accessible?

### 7.2 Is CMA licensing cost and timeline something your funding runway can absorb before launch?

**Answer**

The initial business model is designed so that obtaining full CMA licensing before launch is not a prerequisite.

Version 1 will launch as a technology platform that partners with licensed financial institutions responsible for regulated activities such as brokerage, custody, and trade execution.

This approach allows the company to validate the product, build a customer base, and establish commercial partnerships before evaluating whether obtaining additional licences would provide sufficient strategic value.

As the platform grows, the company will periodically reassess whether bringing regulated activities in-house aligns with its long-term strategy.

**Reason**

Reducing regulatory complexity during the initial launch lowers capital requirements, shortens time to market, and allows the company to focus on delivering a high-quality investment experience. Regulatory expansion should be driven by strategic value rather than becoming a prerequisite for launching the platform.

**Validation Question**

> At what stage of growth would obtaining additional CMA licences become strategically advantageous, and how would the costs, operational responsibilities, and regulatory requirements compare with continuing to partner with licensed financial institutions?
