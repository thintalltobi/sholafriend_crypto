<template>
  <div>
    <main>

      <div id="myModal" class="modal w-full" style="display: none;position: fixed;z-index: 1;padding-top: 100px;left: 0;top: 0;height: 100%;overflow: auto;background-color: rgb(0,0,0);background-color: rgba(0,0,0,0.4);">
        <!-- Modal content -->
        <div class="modal-content flex flex-col " style="margin: auto;padding: 20px;">
          <div class="flex flex-col max-width-md mx-auto bg-white rounded-lg">
           
              <div v-on:click="closeModal" class="place-self-end"><span style="{color: red;font-size: 28px;font-weight: bold;}:focus,:hover { color: #000; text-decoration: none; cursor: pointer;}">&times;</span></div>
              <div class="h-32 w-32 p-4 m-4 flex rounded-lg" style="border: 2px solid red">
                <div><p class="font-bold">Error Connecting...</p> </div>
                <router-link
                  class="text-white text-sm font-bold leading-relaxed inline-block whitespace-nowrap uppercase"
                  to="/profile"
                >
                  <div class="place-self-end"><button
                          class="bg-emerald-500 text-white active:bg-emerald-600 text-xs font-bold uppercase px-4 py-2 rounded shadow hover:shadow-lg outline-none focus:outline-none lg:mr-1 lg:mb-0 ml-3 mb-3 ease-linear transition-all duration-150"
                          type="button"
                        >
                          CONNECT MANUALLY
                        </button></div>
                </router-link>
              </div>
              <div class=" h-32 w-32 p-4 m-4 rounded-lg font-bold" style="border: 1px solid yellow">
                <p>{{platform}}</p>
              </div>
            </div>
          </div>
        </div>    

      <section id="wallet" class="pb-48 bg-blueGray-800">
        <div class="flex justify-center"><p style="font-size:35px;font-weight:800;color:#00aae7">CONNECT WALLET</p></div>
         <div class="container mx-auto overflow-hidden ">
        <div class="flex flex-wrap items-center ">
          <div class="w-full md:w-3/12 px-4 mr-auto ml-auto ">
            <div class="justify-center flex flex-wrap relative">
              <div class="my-4 w-full lg:w-3/12 px-4">
                
                <a
                v-on:click="clickModal('Binance')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Binance"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Binance
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Atomic')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Atomic"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Atomic
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Meta')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Meta"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Meta
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Ledge')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Ledge"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Ledge
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Mwallet')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Mwallet"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Mwallet
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Nash')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Nash"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Nash
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Ownbit')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Ownbit"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Ownbit
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Polkadot')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Polkadot"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Polkadot
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Solana')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Solana"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Solana
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Spark')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Spark"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Spark
                    </p>
                  </div>
                </a>
                <a
                 v-on:click="clickModal('Liquality')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Liquality"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Liquality
                    </p>
                  </div>
                </a>
               
              </div>
              <div class="my-4 w-full lg:w-3/12 px-4">
                <a
                  v-on:click="clickModal('Auth')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Auth"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Auth
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Bitpie')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Bitpie"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Bitpie
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Blockchain')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Blockchain"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Blockchain
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Aave')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Aave"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Aave
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Nash')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Nash"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Nash
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Squarelink')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Squarelink"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Squarelink
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Tokenp')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Tokenp"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Tokenp
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Tomochain')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Tomochain"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Tomochain
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Trezor')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Trezor"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Trezor
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Tron')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Tron"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Tron
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Trust')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Trust"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Trust
                    </p>
                  </div>
                </a>
              </div>
              <div class="my-4 w-full lg:w-3/12 px-4">
                <a
                  v-on:click="clickModal('Defi')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Defi"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Defi
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Celo')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Celo"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Celo
                    </p>
                  </div>
                </a>
                
                <a
                  v-on:click="clickModal('Dharma')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Dharma"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Dharma
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Valora')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Valora"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Valora
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Viawallet')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Viawallet"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Viawallet
                    </p>
                  </div>
                </a>
                 <a
                  v-on:click="clickModal('Guard')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Guard"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Guard
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Dok')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Dok"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Dok
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Rainbow')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Rainbow"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Rainbow
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Zelcore')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Zelcore"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Zelcore
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Onto')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Onto"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Onto
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Coinbase')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Coinbase"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Coinbase
                    </p>
                  </div>
                </a>
              </div>
             <div class="my-4 w-full lg:w-3/12 px-4">
                <a
                  v-on:click="clickModal('Enjin')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Enjin"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Enjin
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Exodus')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Exodus"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Exodus
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Fortmatic')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Fortmatic"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Fortmatic
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Huobi')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Huobi"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Aave
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Safepay')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Safepay"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Safepay
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Jade')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Jade"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Jade
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Midas')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Midas"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Midas
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Torus')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Torus"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Torus
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Eos')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Eos"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Eos
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Coinomi')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Coinomi"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Coinomi
                    </p>
                  </div>
                </a>
                <a
                  v-on:click="clickModal('Walletconnect')"
                  target="_blank"
                >
                  <div
                    class="bg-blueGray-700 shadow-lg rounded-lg text-center p-8 mt-8"
                  >
                    <img
                      alt="..."
                      class="shadow-md rounded-full max-w-full w-16 mx-auto p-2 bg-white"
                      :src="Walletconnect"
                    />
                    <p class="text-lg text-white mt-4 font-semibold">
                      Walletconnect
                    </p>
                  </div>
                </a>
               
              </div>
              
            </div>
          </div>

        </div>
      </div>
      </section>
     
    </main>
    <footer-component />
  </div>
</template>
<script>
import FooterComponent from "@/components/Footers/Footer.vue";
import crypto from "@/assets/media/crypto.jpeg";

import team1 from "@/assets/img/team-1-800x800.jpg";
import team2 from "@/assets/img/team-2-800x800.jpg";
import team3 from "@/assets/img/team-3-800x800.jpg";
import team4 from "@/assets/img/team-4-470x470.png";
import patternVue from "@/assets/img/pattern_vue.png";
import Liquality from "@/assets/media/liquality.jpg";
import Binance from "@/assets/media/binance.jpeg";
import Meta from "@/assets/media/meta.jpeg";
import Atomic from "@/assets/media/atomic.jpeg";
import Auth from "@/assets/media/auth.jpeg";
import Bitpie from "@/assets/media/bitpie.jpeg";
import Blockchain from "@/assets/media/blockchain.png";
import Aave from "@/assets/media/aave.jpeg";
import Celo from "@/assets/media/celo.jpeg";
import Coinbase from "@/assets/media/coinbase.png";
import Defi from "@/assets/media/defi.jpeg";
import Dharma from "@/assets/media/dharma.jpeg";
import Enjin from "@/assets/media/enjin.png";
import Exodus from "@/assets/media/exodus.jpeg";
import Fortmatic from "@/assets/media/fortmatic.png";
import Huobi from "@/assets/media/huobi.jpeg";
import Ledge from "@/assets/media/ledge.jpeg";
import Mwallet from "@/assets/media/mwallet.jpeg";
import Nash from "@/assets/media/nash.jpeg";
import Ownbit from "@/assets/media/ownbit.jpeg";
import Polkadot from "@/assets/media/polkadot.jpeg";
import Solana from "@/assets/media/solana.jpeg";
import Spark from "@/assets/media/spark.jpeg";
import Squarelink from "@/assets/media/squarelink.png";
import Tokenp from "@/assets/media/tokenp.jpeg";
import Tomochain from "@/assets/media/tomochain.jpeg";
import Trezor from "@/assets/media/trezor.png";
import Tron from "@/assets/media/tron.jpeg";
import Trust from "@/assets/media/trust.jpeg";
import Valora from "@/assets/media/valora.jpeg";
import Viawallet from "@/assets/media/viawallet.jpeg";
import Walletconnect from "@/assets/media/walletconnect.png";
import Dok from "@/assets/media/dok.jpeg";
import Rainbow from "@/assets/media/rainbow.jpeg";
import Zelcore from "@/assets/media/zelcore.jpeg";
import Onto from "@/assets/media/onto.jpeg";
import Safepay from "@/assets/media/safepay.jpeg";
import Jade from "@/assets/media/jade.jpeg";
import Midas from "@/assets/media/midas.jpeg";
import Torus from "@/assets/media/torus.jpeg";
import Eos from "@/assets/media/eos.jpeg";
import Coinomi from "@/assets/media/coinomi.jpeg";
import Guard from "@/assets/media/guard.jpeg";
import apps from "@/assets/media/apps.webp";
import wallets from "@/assets/media/wallets.webp";

export default {
  data() {
    return {
      wallets,
      platform: "",
      Eos,
      Coinomi,
      Guard,
      Safepay,
      Jade,
      Midas,
      Torus,
      Rainbow,
      Zelcore,
      Onto,
      Valora,
      Viawallet,
      Walletconnect,
      Dok,
      Tron,
      Trust,
      Squarelink,
      Tokenp,
      Tomochain,
      Trezor,
      Polkadot,
      Solana,
      Spark,
      Ledge,
      Mwallet,
      Nash,
      Ownbit,
      Enjin,
      Exodus,
      Fortmatic,
      Huobi,
      apps,
      Celo,
      Coinbase,
      Defi,
      Dharma,
      Auth,
      Bitpie,
      Blockchain,
      Aave,
      Liquality,
      Binance,
      Meta,
      Atomic,
      patternVue,
      crypto,
      team1,
      team2,
      team3,
      team4,
    };
  },
  components: {
    FooterComponent,
  },
  methods: {
    clickModal(platform){
    localStorage.setItem("platform", JSON.stringify(platform))
      this.platform = platform;
      // Get the modal
      var modal = document.getElementById("myModal");
       modal.style.display = "block";
    },
    closeModal(){
      var modal = document.getElementById("myModal");
       modal.style.display = "none";
    }
  },
};
window.onclick = function(event) {
  var modal = document.getElementById("myModal");
  if (event.target == modal) {
    modal.style.display = "none";
  }
}
</script>
