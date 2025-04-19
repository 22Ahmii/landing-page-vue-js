<template>
    <section class="feedback-section">
        <div class="feedback-inner">
            <div>
                <p class="pre-title">Best time here</p>
                <h2 class="title">Better feedback at the right time.</h2>
            </div>
            <div class="card-main">
                <div class="card-header">
                    <div class="card-info">
                        <img src="../assets/cloud.svg" alt="Cloudhub" class="card-icon" />
                        <div>
                            <div class="card-name">Cloudhub</div>
                            <div class="card-meta">2m ago in Brand</div>
                        </div>
                    </div>
                    <button class="btn-post">View post</button>
                </div>
                <div class="card-body">
                    <div class="avatars">
                        <img src="../assets/pic1.svg" alt="" />
                        <img src="../assets/pic2.svg" alt="" />
                        <img src="../assets/pic3.svg" alt="" />
                    </div>
                    <div class="looking-text">3 people are looking for feedback this week</div>
                </div>
            </div>

            <div class="features">
                <div class="feature">
                    <img src="../assets/icon1.svg" alt="Mentions" class="feature-icon" />
                    <h3>Mentions</h3>
                    <p>Mention anyone on your team to include them in a post.</p>
                </div>
                <div class="feature">
                    <img src="../assets/icon2.svg" alt="Polls" class="feature-icon" />
                    <h3>Polls</h3>
                    <p>Get a quick cut‑check from the team on design options.</p>
                </div>
                <div class="feature">
                    <img src="../assets/icon3.svg" alt="Resolve comments" class="feature-icon" />
                    <h3>Resolve comments</h3>
                    <p>Mark comments as resolved to keep the conversation focused.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>

</script>

<style scoped>
.feedback-section {
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;
    background: linear-gradient(135deg, #ff5722, #ff7043);
    padding: 4rem 0;
    color: #fff;
    box-sizing: border-box;
    margin-top: 60px;
}

.feedback-inner {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 1rem;
    text-align: center;
    border-radius: 1rem;
}

.pre-title {
  margin: 0;              
  margin-bottom: 0.25rem; 
  opacity: 0.8;
}

.title {
  margin: 0;             
  margin-top: 0.25rem;    
  font-size: 2.5rem;
  line-height: 1.2;
  font-weight: 700;
  margin-bottom: 2rem;
}

.card-main {
    background: #1e1e1e;
    border-radius: 0.75rem;
    padding: 3rem;
    height: 200px;
    text-align: left;
}

.card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.card-info {
    display: flex;
    align-items: center;
    gap: 0.75rem;
}

.card-icon {
    width: 2rem;
    height: 2rem;
}

.card-name {
    font-weight: 600;
    font-size: 1.125rem;
}

.card-meta {
    font-size: 0.875rem;
    opacity: 0.7;
}

.btn-post {
    background: #ff5722;
    color: #fff;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 999px;
    cursor: pointer;
    font-weight: 600;
}

.card-body {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-top: 1.25rem;
}

.avatars {
    display: flex;
    margin-left: -0.5rem;
}

.avatars img {
    width: 2rem;
    height: 2rem;
    border-radius: 50%;
    border: 2px solid #1e1e1e;
    margin-left: -0.5rem;
}

.looking-text {
    font-size: 0.875rem;
    opacity: 0.8;
}

.features {
    display: flex;
    gap: 1rem;
    margin-top: 2rem;
}

.feature {
    background: #1e1e1e;
    flex: 1;
    border-radius: 0.75rem;
    padding: 1rem;
    text-align: left;
}

.feature-icon {
    width: 1.5rem;
    height: 1.5rem;
    margin-bottom: 0.75rem;
}

.feature h3 {
    margin: 0;
    font-size: 1rem;
    font-weight: 600;
    margin-bottom: 0.5rem;
}

.feature p {
    margin: 0;
    font-size: 0.875rem;
    opacity: 0.8;
}


@media (max-width: 768px) {
    .card-main {
        padding: 1rem;
    }

    .card-body {
        flex-direction: column;
        align-items: flex-start;
    }

    .features {
        flex-direction: column;
    }
}
</style>