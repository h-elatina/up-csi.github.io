<script>
    import CardContainer from '$lib/components/panels/CardContainer.svelte';
    import CartoonCard from '$lib/components/cards/CartoonCard.svelte';
    import ContactUs from '$lib/components/contacts/ContactUs.svelte';
    import HeroLanding from '$lib/components/headers/HeroLanding.svelte';
    import WhoWeAre from '$lib/components/headers/WhoWeAre.svelte';
    import devcamps from '$lib/assets/cartoons/devcamps.svg';
    import services from '$lib/assets/cartoons/cartoon-card-placeholder.svg';
    import tech from '$lib/assets/cartoons/tech.svg';
</script>

<HeroLanding />
<WhoWeAre />

<section class="prose">
    <h1 class="text-csi-blue-600 text-center text-5xl font-normal transition-colors ease-in-out">
        Why UP CSI?
    </h1>
    <div class="space-y-4">
        <CardContainer>
            {#snippet text()}
                <p class="text-csi-blue-600 text-3xl">For organizations</p>
                <hr class="border-csi-blue-600 border-t-2" />
                <h3 class="font-dm text-2xl font-normal sm:text-3xl">
                    We offer services catered to your specific software needs.
                </h3>
                <p class="leading-5 sm:leading-6">
                    Need a small site or a full-scale project? Contact us to see how we can help.
                </p>
            {/snippet}
            {#snippet cards()}
                <CartoonCard src={services}></CartoonCard>
            {/snippet}
        </CardContainer>
        <CardContainer>
            {#snippet text()}
                <p class="text-csi-blue-600 text-3xl">For students</p>
                <hr class="border-csi-blue-600 border-t-2" />
                <h3 class="font-dm text-2xl font-normal sm:text-3xl">
                    We enhance and upskill student abilities.
                </h3>
                <p class="leading-5 sm:leading-6">
                    From training programs to external workshops, we elevate students' development
                    skills.
                </p>
            {/snippet}
            {#snippet cards()}
                <CartoonCard src={devcamps}>Developer Training Program & DevCamp</CartoonCard>
                <CartoonCard src={tech}>Technology Workshops</CartoonCard>
            {/snippet}
        </CardContainer>
    </div>
</section>

<ContactUs />
