<script>
    import Navbar from "$lib/shared/ui/components/navbar/Navbar.svelte";
    import Footer from "$lib/shared/ui/components/footer/Footer.svelte";

    import { redirect } from "@sveltejs/kit";
	import { goto } from "$app/navigation";
</script>

<main class="main-container">
    <Navbar />
    <div class="background-gradient"></div>
    <div class="background-image">
        <img src="/src/assets/webpagebg_2.png" alt="Petrichor Background" />
    </div>
	<div class="petrichor-logo">
        <img src="/src/assets/petrichor_1.png" alt="Petrichor Logo" />
	</div>
    <div class="text">
        <div class="heading">
            Petrichor' 26
        </div>
        <div class="description">
            The Annual Techno-Cultural Fest of IIT Palakkad
        </div>
        <div class="buttons">
            <button class="discover" onclick={()=>{goto ("/discover")}}>
                <div class="discover_text">
                    Discover More
                </div>
            </button>
            <button class="caportal" onclick={()=>{goto ("/ca")}}>
                <div class="ca_text">
                    CA Portal
                </div>
            </button>
        </div>
    </div>
    <Footer />
</main>

<style>
    .main-container {
		padding: 0px;
		width:1440px;
		height: 1009px;
	}
    
    .background-gradient {
        position: absolute;
        top: 0px;
        left: 0px;
        width: 1440px;
        height: 1009px;
        z-index: -2;
        background: linear-gradient(195deg, #01e8fa -30%, #01cff7 -17%, #01d6f4 -5%, #039ff1 7%, #074f88 21%, #005698 33%, #001423 50%, #000910 65%);
    }

    .background-image {
        position: absolute;
        top: 97px;
        left: 820px;
        width: 613.578px;
        height: 836px;
        z-index: -1;
    }

    .petrichor-logo {
        position: absolute;
        top: 100px;
        left: 180px;
        display: flex;
        height: 369px;
        width: 369px;
        align-items: center;
        justify-content: center;
    }

    .text {
        margin-top: 360px;
        padding-left: 70px;
        display: flex;
        flex-direction: column;
        margin-left: 50px;
        color: #ffffff;
    }

    .heading {
        width: 783px;
        height: 91px;
        font-family: "Cormorant SC";
        font-weight: bold;
        font-size: 86px;
    }

    .description {
        width: 568px;
        height: 22px;
        margin-top: 20px;
        font-family: "Inter";
        font-size: 24px;
    }

    .buttons {
        display: flex;
        flex-direction: column;
        width: 500px;
        align-items: center;
        justify-content: center;
    }

    .discover {
        margin-top: 50px;
        height: 76px;
        width: 230px;
        border-width: 1px;
        border-color: #7ec8fd;
        border-radius: 20px;
        cursor: pointer;
        align-items: center;
        justify-content: center;
        background: linear-gradient(90deg, #7ec8fd, #00101c);
    }

    .discover_text {
        height: 36px;
        width: 166px;
        margin-left: 32px;
        font-family: "Inter";
        font-size: 24px;
        color: #ffffff;
        align-items: center;
        justify-content: center;
    }

    .caportal {
        margin-top: 20px;
        height: 76px;
        width: 173px;
        border-width: 1px;
        border-color: #7ec8fd;
        border-radius: 20px;
        cursor: pointer;
        align-items: center;
        justify-content: center;
        background: linear-gradient(90deg, #7ec8fd, #00101c);
    }

    .ca_text {
        height: 36px;
        width: 109px;
        margin-left: 32px;
        font-family: "Inter";
        font-size:24px;
        color: #ffffff;
        align-items: center;
        justify-content: center;
    }
</style>