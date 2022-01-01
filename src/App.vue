<template>
  <div class="full-screen">
    <wallet-provider :wallets="wallets" auto-connect>
        <div>
            <div class="fixed top-0 right-0 p-8">
                <wallet-modal-provider>
                    <wallet-multi-button></wallet-multi-button>
                </wallet-modal-provider>
            </div>
        </div>
    </wallet-provider>
  </div>
</template>

<script setup>
  import {
      getPhantomWallet,
  } from '@solana/wallet-adapter-wallets'
  import { WalletProvider } from '@solana/wallet-adapter-vue'
  import { WalletMultiButton, WalletModalProvider } from '@solana/wallet-adapter-vue-ui'

  require("@solana/wallet-adapter-vue-ui/styles.css");

  const wallets = [
      getPhantomWallet(),
  ]
</script>
