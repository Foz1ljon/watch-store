<script>
export default {
  data() {
    return {
      datas: [
        {
          img: "/apple.png",
          title: "Apple",
          about:
            "Apple is one of the most famous smart watches providing company.",
        },
        {
          img: "/xiaomi.png",
          title: "Xiaomi",
          about: "Xiaomi smart watches are produced by MI company.",
        },
        {
          img: "/fitbit.png",
          title: "FitBit",
          about:
            "FitBit smart watches are best for there health and fitness features.",
        },
      ],
      products: [
        {
          img: "/1.png",
          title: "Apple Smart I",
          reting: "/rating.svg",
          old_price: "$300",
          new_price: "$255.00",
        },
        {
          img: "/2.png",
          title: "Apple Smart II",
          reting: "/rating.svg",
          old_price: "$300",
          new_price: "$255.00",
        },
        {
          img: "/3.png",
          title: "Apple Smart III",
          reting: "/rating.svg",
          old_price: "$300",
          new_price: "$255.00",
        },
        {
          img: "/4.png",
          title: "Apple Smart VI",
          reting: "/rating.svg",
          old_price: "$300",
          new_price: "$399.00",
        },
        {
          img: "/5.png",
          title: "Samsung Watch Pro",
          reting: "/rating.svg",
          old_price: "$300",
          new_price: "$255.00",
        },
        {
          img: "/6.png",
          title: "FitBit Max 1",
          reting: "/rating.svg",
          old_price: "",
          new_price: "$155.00",
        },
      ],
      says: [
        {
          img: "/user1.png",
          title: "Hamza Faizi",
          about:
            "Don’t waste time, just order! This is the best website to puschase smart watches.",
          rating: "/rating.svg",
        },
        {
          img: "/user2.png",
          title: "Hafiz Huzaifa",
          about:
            "I’ve been purchasing smart watches of Mohid for a long time. All the products are good quality.",
          rating: "/rating.svg",
        },
      ],
    };
  },
  methods: {},
};
</script>

<template>
  <div class="bg-black">
    <div class="container">
      <!-- Navbar start>>>>>>>>  -->
      <nav class="flex justify-between items-center">
        <div class="log"><img src="/logo.svg" alt="logo" /></div>
        <div class="menu text-[#8B8E99] flex gap-4">
          <a href="#home">Home</a>
          <a href="#brands">Brands</a>
          <a href="#ntrece">Recent Products</a>
          <a href="#contact">Contact</a>
          <a href="#about">About</a>
        </div>
        <div class="btns flex gap-2">
          <button><img src="/search.svg" alt="" /></button>
          <button><img src="/person.svg" alt="" /></button>
          <button><img src="/shopping.svg" alt="" /></button>
        </div>
      </nav>
      <!-- Navbar end>>>>>>>>  -->

      <!-- Hero start>>>>>>>>  -->

      <main class="flex justify-between items-center py-14">
        <div class="about flex flex-col gap-10">
          <h1 class="text-6xl text-white font-semibold w-[500px]">
            Discover <br />
            Most Suitable Watches
          </h1>
          <p class="text-[16px] text-[#8B8E99] w-[400px]">
            Find the best, reliable, and cheap smart watches here. We focus on
            product quality. Here you can find smart watches of almost all
            brands. So why you are waiting? Just order now!
          </p>
          <div class="input relative">
            <input
              type="text"
              class="py-4 px-16 rounded-md"
              placeholder="Find the best brands "
            />
            <button
              class="py-2 px-4 bg-[#3858D6] text-white rounded-md absolute top-2 right-[27%]"
            >
              Search
            </button>
          </div>
        </div>
        <img src="/img.png" alt="" />
        .
      </main>
      <!-- Hero start>>>>>>>>  -->
    </div>
  </div>

  <div class="container">
    <div class="flex justify-between py-14">
      <div v-for="(item, index) in datas">
        <div
          :key="index"
          class="flex gap-10 bg-[#F6F6F6] px-5 py-5 w-[335px] items-center rounded-lg"
        >
          <div class="img"><img :src="item.img" alt="apple-img" /></div>
          <div class="flex flex-col">
            <h1 class="text-3xl font-medium">{{ item.title }}</h1>
            <p class="text-[16px] text-[#8B8E99] w-[173px]">
              {{ item.about }}
            </p>
          </div>
        </div>
      </div>
    </div>

    <section>
      <div class="flex flex-col gap-[1px] items-center mt-20 mb-14">
        <p class="text-[14px] text-[#3858D6] font-medium">
          Find your favourite smart watch.
        </p>
        <h1 class="text-4xl font-bold">Our Latest Products</h1>
      </div>
      <div class="grid grid-cols-3 gap-2 grid-rows-2">
        <div v-for="(item, index) in products">
          <!--  -->

          <div
            :key="index"
            class="card flex flex-col w-[335px] justify-center items-center"
          >
            <div class="cart group flex bg-[#F6F6F6] p-12 relative">
              <img :src="item.img" alt="" />
              <div
                class="btns flex-col gap-2 absolute right-3 top-2 hidden group-hover:flex"
              >
                <button
                  class="bg-[#3858D6] w-[35px] h-[35px] p-1 rounded-full flex justify-center items-center"
                >
                  <img src="/cart.svg" alt="" />
                </button>
                <button
                  class="bg-[#FF6B6B] w-[35px] h-[35px] p-1 rounded-full flex justify-center items-center"
                >
                  <img src="/like.svg" alt="" />
                </button>
              </div>
            </div>

            <div class="items-center flex flex-col gap-2">
              <h1 class="text-[24px] font-medium">{{ item.title }}</h1>
              <img class="w-20" :src="item.reting" alt="" />
              <div class="flex gap-5">
                <p class="text-[#8B8E99] text-2xl line-through">
                  {{ item.old_price }}
                </p>
                <p class="text-2xl font-medium">{{ item.new_price }}</p>
              </div>
            </div>
          </div>

          <!--  -->
        </div>
      </div>
      <center>
        <button
          class="py-2 px-6 border bg-[#3858D6] text-white rounded-xl my-10"
        >
          View more
        </button>
      </center>
    </section>

    <section>
      <div class="flex flex-col gap-[1px] items-center mt-20 mb-14">
        <p class="text-[14px] text-[#3858D6] font-medium">
          Here are our some of the best clients.
        </p>
        <h1 class="text-4xl font-bold">What People Say About Us</h1>
      </div>

      <div class="cards flex justify-between">
        <div v-for="(item, index) in says">
          <div class="card flex bg-[#F6F6F6] rounded-md p-3 px-7 items-center">
            <div class="p-4">
              <img :src="item.img" width="162" alt="user" />
            </div>
            <div class="about flex flex-col gap-2">
              <h1 class="text-2xl font-medium">{{ item.title }}</h1>
              <p class="text-[16px] text-[#8B8E99] w-[250px]">
                {{ item.about }}
              </p>
              <img class="w-[50%]" :src="item.rating" alt="" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div
        class="wrapper flex justify-between items-center px-20 py-3 bg-[#F6F6F6] my-20 mt-30"
      >
        <div class="flex flex-col gap-2">
          <h1 class="text-4xl font-bold">Our Latest Products</h1>
          <p class="text-[14px] text-[#3858D6] font-medium">
            Find your favourite smart watch.
          </p>
          <div class="input relative mt-2">
            <input
              type="text"
              class="py-4 px-16 rounded-md"
              placeholder="Enter email address"
            />
            <button
              class="py-2 px-4 bg-[#3858D6] text-white rounded-md absolute top-2 right-[3%]"
            >
              Subscribe
            </button>
          </div>
        </div>
        <div class="img"><img src="/1.png" width="272" alt="" /></div>
      </div>
    </footer>
  </div>
  <div class="w-full flex justify-center bg-black text-white py-4">
    Copyright @ 2022 | Mohid
  </div>
</template>

<style scoped></style>
