<template>
  <div class="py-4 container-fluid">
    <div class="row">
      <div class="col-lg-16">
        <div class="row">
          <div class="col-lg-6 mb-lg">
            <confusion-matrix />
          </div>
          <div class="col-lg-6">
            <div class="row">
              <percentage-accuracy />
            </div>
            <div class="row mt-3">
              <classification-report />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

import PercentageAccuracy from "./components/PercentageAccuracy.vue";
import ConfusionMatrix from "./components/ConfusionMatrix.vue";
import ClassificationReport from "./components/ClassificationReport.vue";
import US from "@/assets/img/icons/flags/US.png";
import DE from "@/assets/img/icons/flags/DE.png";
import GB from "@/assets/img/icons/flags/GB.png";
import BR from "@/assets/img/icons/flags/BR.png";

export default {
  name: "dashboard-default",
  data() {
    return {
      count: null,
			positiveSentiment: null,
			negativeSentiment: null,
			hashtag: null,
			posneg: null,
			loadingCount: false,
			loadingNegativeSentinment: false,
			loadingPositiveSentiment:false,
			loadingChart:false,
      stats: {
        tweet: {
          title: "Number of tweets",
          value: "$53,000",
          iconClass: "fas fa-comment",
          iconBackground: "bg-gradient-primary",
        },
        positive: {
          title: "Positive Sentiment",
          value: "2,300",
          iconClass: "fas fa-plus",
          iconBackground: "bg-gradient-success",
        },
        negative: {
          title: "Negative Sentiment",
          value: "+3,462",
          iconClass: "fas fa-times",
          percentageColor: "text-danger",
          iconBackground: "bg-gradient-danger",
        },
        accuracy: {
          title: "Accuarcy",
          value: "82.5 %",
          iconClass: "ni ni-paper-diploma",
          iconBackground: "bg-gradient-warning",
        },
      },
      sales: {
        us: {
          country: "United States",
          sales: 2500,
          value: "$230,900",
          bounce: "29.9%",
          flag: US,
        },
        germany: {
          country: "Germany",
          sales: "3.900",
          value: "$440,000",
          bounce: "40.22%",
          flag: DE,
        },
        britain: {
          country: "Great Britain",
          sales: "1.400",
          value: "$190,700",
          bounce: "23.44%",
          flag: GB,
        },
        brasil: {
          country: "Brasil",
          sales: "562",
          value: "$143,960",
          bounce: "32.14%",
          flag: BR,
        },
      },
    };
  },
  created() {
		this.hashtag = "vaksin";
	},
  components: {
    ClassificationReport,
    ConfusionMatrix,
    PercentageAccuracy,
  },
  
};
</script>
