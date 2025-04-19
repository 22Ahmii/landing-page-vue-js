<template>
    <section class="visibility-section">
        <div class="visibility-inner">
            <img src="../assets/logodemo.svg" alt="Visibility Icon" class="visibility-icon" />
            <h2 class="visibility-title">Increase your team’s visibility and alignment</h2>
            <p class="visibility-subtitle">Start for free, flexible for all teams.</p>
            <div class="visibility-ctas">
                <a href="#" class="demo-link">Request a demo</a>
                <button class="free-btn">Start for free</button>
            </div>
        </div>
    </section>
</template>

<script setup>
// Static section for visibility and alignment
</script>

<style scoped>
.visibility-section {
    width: 100%;
    padding: 4rem 1rem;
}

.visibility-inner {
    max-width: 600px;
    margin: 0 auto;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.5rem;
}

.visibility-icon {
    width: 3rem;
    height: 3rem;
}

.visibility-title {
    font-size: 2rem;
    font-weight: 700;
    margin: 0;
    white-space: nowrap; /* prevent wrapping, keep text in one line */
}

.visibility-subtitle {
    font-size: 1rem;
    opacity: 0.9;
    margin: 0;
}

.visibility-ctas {
    display: flex;
    align-items: center;
    gap: 1.5rem;
}

.demo-link {
    text-decoration: none;
    color: black;
    font-weight: 600;
}

.free-btn {
    background: #ff5630;
    color: #fff;
    font-weight: 600;
    border: 0;
    padding: .9rem 2.2rem;
    border-radius: 999px;
    cursor: pointer;
    transition: transform .2s ease;
}

/* Responsive */
@media (max-width: 768px) {
    .visibility-title {
        font-size: 1.75rem;
    }

    .visibility-ctas {
        flex-direction: column;
        gap: 1rem;
    }

    .free-btn {
        width: 100%;
    }
}
</style>