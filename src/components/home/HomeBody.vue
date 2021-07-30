<template>
  <section>
    <div class="home__body">
      <b-container>
        <div id="about" class="home__body-about">
          <h2 class="font-weight-bold">About us</h2>
          <p class="font-weight-bold">
            Everstake Capital was created as a branch firm of the well-known Everstake.one - top
            tier POS validator company in many POS public blockchains.
          </p>
        </div>

        <ul class="row home__body-about-list">
          <li class="col-lg-6 col-md-12">
            Everstake Capital is a private umbrella fund structure in the form of a segregated
            portfolio company.
          </li>
          <li class="col-lg-5 col-md-12">
            Sound tech background and strong blockchain expertise is our secret sauce to identify
            new promising projects, anticipate revolutionary innovations impacting open markets,
            maximize investment returns and mitigate the underlying risks.
          </li>
          <li class="col-lg-6 col-md-12">
            Everstake Capital provides wide access to blockchain-based assets both at early-stage
            and up to already existing already established projects.
          </li>
          <li class="col-lg-5 col-md-12">
            Everstake Capital provides institutional grade investment services mainly focused on POS
            and DEFI markets.
          </li>
        </ul>
      </b-container>

      <div id="sector" class="home__body-target-sectors">
        <b-container class="home__body-sector">
          <h2 class="font-weight-bold mb-5">Target Sectors</h2>
          <div class="d-flex justify-content-between">
            <span>Platform</span>
            <span>DeFi</span>
            <span>Index funds</span>
            <span>Staking</span>
            <span>Farming</span>
          </div>
        </b-container>
      </div>

      <b-container id="advantages" class="mt-5">
        <h2 class="mb-4 font-weight-bold">Company advantages</h2>

        <ul class="d-flex flex-column home__body-advantage">
          <li>our investment style based on deep market analytics</li>
          <li>scientific approach</li>
          <li>market reputation</li>
          <li>established business model</li>
          <li>global outreach</li>
          <li>solid operating structure</li>
          <li>in-house comprehensive due diligence expertise</li>
        </ul>

        <MediaList />
      </b-container>
    </div>
  </section>
</template>

<script>
import MediaList from '../MediaList.vue';

export default {
  name: 'HomeBody',
  components: { MediaList },
};
</script>

<style lang="scss" scoped>
.home {
  &__body {
    display: flex;
    flex-direction: column;
    margin-top: 64px;

    & h2 {
      font-size: $fs48;
    }

    & ul {
      list-style: square;
    }

    &-target-sectors {
      background-color: $white-smoke;
      margin-bottom: 84px;

      & span {
        font-weight: 500;
        font-size: $fs24;
      }
    }

    &-about {
      margin-bottom: 110px;

      &-list {
        gap: 3rem;
        margin-bottom: 120px;
      }
    }

    &-sector {
      padding: 54px 0 73px;
    }

    &-advantage {
      row-gap: 3rem;
      margin-bottom: 159px;
    }

    @include xl-down {
      & h2 {
        font-size: $fs36;
      }

      & span {
        font-size: $fs18;
      }
    }
  }
}
</style>
