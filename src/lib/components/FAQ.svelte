<script lang="ts">
    let openIndex: number | null = 0;

    const faqs = [
        { q: "What makes Calamos different from other asset managers?", a: "Calamos has specialized in convertible securities for over 47 years, making us the leading global asset manager in this space. Our proprietary capital structure analysis examines equity, debt, and convertibles across the entire spectrum—a methodology developed by our founder, a former Air Force pilot who applied aviation risk management principles to investing. With $46+ billion in AUM and an institutional-grade research infrastructure, we deliver sophisticated strategies that were traditionally available only to institutional investors." },
        { q: "What are convertible securities and why are they important?", a: "Convertible securities are hybrid instruments that combine features of both bonds and stocks. They offer downside protection through their bond-like characteristics while providing upside participation through conversion to equity. Our founder, John P. Calamos Sr., recognized through decades of market cycles that convertibles offer superior risk-adjusted returns—protecting capital during downturns while capturing gains during rallies." },
        { q: "How does Calamos serve Registered Investment Advisors (RIAs)?", a: "We partner with RIAs by providing access to institutional-grade alternative investment strategies that help advisors serve sophisticated clients. Through industry conferences and educational workshops, we simplify complex alternative investments and provide the research infrastructure, risk management tools, and proven track record that RIAs need to confidently recommend our strategies." },
        { q: "What is your investment philosophy?", a: "Our philosophy is rooted in rigorous preparation and disciplined risk assessment. As our founder said, 'Investing is like flying an airplane—you better do your homework before you take off.' We practice active management with emphasis on risk mitigation, using our proprietary capital structure analysis to identify opportunities others miss. We don't follow trends—we create them." },
        { q: "What types of investment strategies does Calamos offer?", a: "We offer a diversified range of strategies including convertible securities, alternative investments, structured products, equity strategies, and fixed income solutions. All are built on our core competency of capital structure analysis and designed to provide institutional-grade sophistication with accessibility for individual investors through their advisors." },
        { q: "How large is Calamos and how long have you been in business?", a: "Calamos was founded in 1977 and has grown to manage over $46 billion in assets. We've navigated 47+ years of market cycles, from the founder's initial boutique convertible securities practice to today's diversified global investment firm. This longevity demonstrates our ability to adapt and deliver value through changing market conditions." },
        { q: "Who leads Calamos today?", a: "John Koudounis serves as CEO with a clear vision: 'Lead the charge in innovation, deliver excellence to our clients and make Calamos the premier alternative management brand.' The family legacy continues with multi-generational leadership involvement, maintaining the founder's disciplined approach while driving innovation." },
        { q: "What is your approach to risk management?", a: "Risk management is embedded in our DNA. Our founder's aviation background taught him that rigorous preparation and risk assessment are non-negotiable. We apply this discipline through comprehensive capital structure analysis, active portfolio management, and systematic risk monitoring. Our goal is to protect capital while capturing upside—delivering superior risk-adjusted returns across market cycles." },
        { q: "How does Calamos democratize institutional-grade strategies?", a: "We've built distribution partnerships with RIAs to bring sophisticated strategies to individual investors. By providing educational resources, simplifying complex products, and offering institutional research infrastructure, we make alternative investments accessible to advisors and their clients—expanding beyond the traditional institutional-only model." },
        { q: "What is your track record during market volatility?", a: "Our founder experienced decades of market cycles and volatility firsthand, which gave him deep conviction in convertible securities' ability to deliver superior risk-adjusted returns. Our 47+ year history includes navigating multiple recessions, market crashes, and recovery periods. This experience informs our active management approach and risk mitigation strategies." },
        { q: "How do I get started with Calamos as a financial advisor?", a: "We welcome partnerships with RIAs seeking sophisticated investment solutions for their clients. Connect with us through our contact form, attend one of our industry conferences, or join our educational workshops on alternative investments. Our team will work with you to understand your clients' needs and demonstrate how our strategies can enhance your practice." },
        { q: "What research capabilities support your investment process?", a: "We maintain an institutional-grade research infrastructure with dedicated portfolio managers, research analysts, and trading specialists. Our in-house team conducts fundamental analysis using our proprietary capital structure framework, supported by advanced technology and risk management systems developed over nearly five decades." },
    ];

    function toggle(index: number) {
        openIndex = openIndex === index ? null : index;
    }
</script>

<section class="bg-gray-50 text-black px-6 md:px-12 py-24">
    <div class="max-w-7xl mx-auto">
        <h2 class="text-3xl font-medium mb-12">Frequently Asked Questions</h2>
        
        <div class="border-t border-black/10">
            {#each faqs as faq, i}
                <div class="border-b border-black/10">
                    <button 
                        class="w-full py-6 flex justify-between items-center text-left hover:text-gray-600 transition-colors"
                        onclick={() => toggle(i)}
                        aria-expanded={openIndex === i}
                    >
                        <span class="text-lg font-light pr-8">{faq.q}</span>
                        <span class="text-xl font-light">{openIndex === i ? '×' : '+'}</span>
                    </button>
                    {#if openIndex === i}
                        <div class="pb-6 text-gray-700 font-light leading-relaxed max-w-4xl">
                            {faq.a}
                        </div>
                    {/if}
                </div>
            {/each}
        </div>
    </div>
</section>