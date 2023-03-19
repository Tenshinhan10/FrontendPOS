<template>
  <div>
    <div>
      <b-navbar toggleable="lg" type="dark" variant="secondary">
        <b-navbar-brand href="#">POS Shop</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-form>
                <b-button size="sm" class="my-2 my-sm-0" href="/home" style="margin-right:5px"
                >Home</b-button>
                <b-button size="sm" class="my-2 my-sm-0" href="/" style="margin-right:5px"
                >Product</b-button>
                <b-button size="sm" class="my-2 my-sm-0" href="/login" style="margin-right:5px"
                >➜</b-button>
            </b-nav-form>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>

    <b-container>
      <Nuxt />
    </b-container>

  </div>
</template>

<script>
export default {};
</script>

<style scoped
</style>