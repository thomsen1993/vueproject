
import BorderedImage from '@/components/BorderedImage.vue';
<template>
    <main class="grid-2-cols">
        <form action="">
            <div>
                <h1>Contact us</h1>
                <p class="sub-title">Subheading for description or instructions</p>
            </div>
            <div class="grid-2-cols names">
                <div>
                    <label for="fName">First name</label> <br>
                    <input type="text" name="" id="fName" placeholder="Jane">
                </div>
                <div>
                    <label for="fName">Last name</label> <br>
                    <input type="text" name="" id="lName" placeholder="Smiktherton">
                </div>
            </div>
            <div>
                <label for="email">Email address</label> <br>
                <input type="email" name="" id="email" placeholder="email@janesfakedomain.net">
            </div>
            <div>
                <label for="message">You message</label> <br>
                <textarea name="" id="" rows="5" placeholder="Enter your question or message"></textarea>
            </div>
        </form>
        <BorderedImage src="../../public/assets/images/b.jpg"/>
    </main>
</template>

<script>
import BorderedImage from "@/components/BorderedImage.vue";

export default {
  components: {
    BorderedImage,
  }
}
</script>

<style scoped>
.grid-2-cols {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: 2rem;
}

.sub-title {
    margin-top: 1rem;
}

.names {
    margin-top: 3rem;
}

form {
    margin: auto 0;
    z-index: 1;
}

input {
    width: 100%;
    padding: 10px 5px;
    margin: 1rem 0;
}

textarea {
    padding: 10px 5px;
    margin: 1rem 0;
    width: 100%;
    resize: none;
}

img {
    width: 100%;
    height: auto;
}
</style>