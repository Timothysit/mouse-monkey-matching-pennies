---
title: Monkey and mouse matching pennies
theme: neversink
info: |
  Timothy Sit
neversink_slug: Mokey and mouse matching pennies
neversink_string: "Neversink Example Deck"
background: https://cover.sli.dev
colorSchema: light
routerMode: hash
transition: fade-out
drawings:
  persist: false
mdc: true
layout: cover
---


<h1 class="text-left-align">
  Monkey and mouse <br> matching pennies
</h1>


Timothy Sit <br>
2025-11-21



---
transition: fade-out
layout: default
---

# Outline

<div pt-35> 

1. Mouse and monkey matching pennies task 
2. Mouse and monkey matching pennies behaviour analysis 
3. Mouse vs mouse matching pennies

</div>


---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# Monkey and mice learn matching pennies 

:: left :: 

## Monkey 


<div>
  <img v-if="$clicks === 1" src="/D_lee_block_transition_p_right_plots.png" class="w-[90%]" />
  
  <img v-else-if="$clicks >= 2" src="/monkey_dataset_1_choose_right.svg" class="w-[100%]" />
</div>


<div v-if="$clicks >= 1">

Data from Lee 2004 - Reinforcement learning and decision making in monkeys during a competitive game.

</div>


:: right :: 

## Mouse 

<div v-click="3" class="flex justify-center">
  <img src="/example_naive_exprt_choices.png" class="opacity-100 w-[50%]"/>
</div>

<div v-click="4" class="flex justify-center" style="width: 100%">
  <img 
    src="/learning_summary_horizontal.png" 
    class="opacity-100" 
    style="
      clip-path: inset(0 34% 0 0); 
      transform: scale(1.5); 
      transform-origin: top left;
      height: 100%; 
      width: auto; 
    "
  />
</div>


---
transition: fade-out 
layout: two-cols-title 
columns: is-5
---

:: title :: 

# Clustering behaviour into states via GLM-HMM 

:: left :: 

## Model



<img src="/GLM-HMM-cartoon_v1.svg" class="opacity-100 w-[100%]" v-click="1"/>


:: right :: 

## Verification with synthetic data 


<img src="/recovered_glm_weights_4_states.svg" class="opacity-100 w-[100%]" v-click="3"/>


<img src="/p_state_4_states.svg" class="opacity-100 w-[100%]" v-click="2"/>


<div v-click="1" class="absolute bottom-40 left-12 w-[35%] text-sm opacity-75">
  <hr class="border-t border-gray-600 opacity-0 mb-2" />
  
  > Generalised linear model - Hidden Markov Model (GLM-HMM) from Ashwood 2022: Mice alternate between discrete strategies during perceptual decision-making
</div>




---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# Clustering behaviour into states via GLM-HMM 


:: left :: 

## Monkey

<img src="/delta_logloss_per_state_balanced_trials_per_algorithm.svg" class="opacity-100 w-[55%]" v-click="3"/>

<img src="/monkey_three_states_weight_v2.svg" class="opacity-100 w-[100%]" v-click="3"/>



:: right :: 

## Mouse

<img src="/glmhmm_CV_delta_test_ll.svg" class="opacity-100 w-[50%]" v-click="1"/>


<img src="/clustered_glm_weights_cosyneabstract2025.svg" class="opacity-100 w-[100%]" v-click="2"/>


<div v-click="4"
     class="absolute bottom-50 left-80 w-[35%] 
            bg-yellow-200/90 text-black text-lg font-semibold 
            p-4 rounded-xl shadow-xl leading-snug">
  Both mouse and monkey's behaviour can be characterised into 3 states,  
  with a common stochastic state
</div>


---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# GLM-HMM states over sessions

:: left :: 


## Monkey


<div class="relative w-full h-[500px] mt-0">
  <!-- Image 1: visible on click 3 only -->
  <img
    src="/C_state_probabilities_per_session.png"
    class="opacity-100 w-[100%] absolute inset-0"
    v-click="3"
    v-click-hide="6"
  />

  <!-- Image 2: visible on click 4 only -->
  <img
    src="/E_state_probabilities_per_session.png"
    class="opacity-100 w-[100%] absolute inset-0 mt-30"
    v-click="4"
    v-click-hide="6"
  />

  <!-- Image 3: visible on click 5 only -->
  <img
    src="/F_state_probabilities_per_session.png"
    class="opacity-100 w-[100%] absolute inset-0 mt-60"
    v-click="5"
    v-click-hide="6"
  />

  <!-- Image 4: visible from click 6 onwards -->
  <img
    src="/monkey_ave_p_state_over_algorithms.png"
    class="opacity-100 w-[100%] absolute inset-0 mt-20"
    v-click="6"
  />
</div>

:: right ::


<div v-click="2">
  <img src="/monkey_three_states_weight_v2.png" class="opacity-100 w-[100%]"/>
</div>



## Mouse


<div v-click="1" class="absolute top-[70%] left-120 w-[70%] -translate-y-1/2">
  <img src="/average_pstate_smooth_cosyneabstract2025.svg" class="opacity-100 w-[50%]"/>
</div>


<div v-click="7"
     class="absolute bottom-50 left-80 w-[35%] 
            bg-yellow-200/90 text-black text-lg font-semibold 
            p-4 rounded-xl shadow-xl leading-snug">
  In monkeys, the transition between states corresponds well with the 3 computer algorithms.
  In mice, there is a general increase in stochastic states over training.
</div>



---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# We can relate states to other behavioural measures 


:: left :: 

## Monkey 

<div v-click="1">
  <img src="/monkey_three_states_weight.png" class="opacity-100 w-[100%]"/>
</div>

<div class="relative w-full h-[150px] kde-reveal">
  <!-- Step 1 & 2: left 1/3 visible -->
  <img
    src="/monkey_kde_per_state.png"
    class="absolute inset-0 w-full h-full object-contain kde-left-third"
    v-click="[3,5]"
  />

  <!-- Step 2: right 1/3 visible (so left + right at click 8) -->
  <img
    src="/monkey_kde_per_state.png"
    class="absolute inset-0 w-full h-full object-contain kde-right-third"
    v-click="[4,5]"
  />

  <!-- Step 3: full image -->
  <img
    src="/monkey_kde_per_state.png"
    class="absolute inset-0 w-full h-full object-contain"
    v-click="5"
  />
</div>

<style>
/* Only affects this slide’s container */
.kde-reveal .slidev-vclick-hidden {
  display: none;
}

/* Left 1/3 of the image */
.kde-left-third {
  clip-path: inset(0 61% 0 0);
}

/* Right 1/3 of the image */
.kde-right-third {
  clip-path: inset(0 0 0 68.7%);
}

/* Only affects this slide’s container */
.mouse-kde-reveal .slidev-vclick-hidden {
  display: none;
}

/* Left 1/3 of the image */
.mouse-kde-left-third {
  clip-path: inset(0 69% 0 0);
}

/* Right 1/3 of the image */
.mouse-kde-right-third {
  clip-path: inset(0 0 0 56%);
}
</style>

<div v-click="1" class="absolute bottom-5 left-12 w-[45%] text-sm opacity-75">
  <hr class="border-t border-gray-600 opacity-0 mb-2" />
  
  > P(WSLS) calculated as $P(X_t = Y_{t-1})$ where <br> $X_t$ and $Y_t$ are the animal’s and opponent’s choices on trial $t$.
</div>

:: right :: 

## Mouse 

<div v-click="2">
  <img src="/clustered_glm_weights_cosyneabstract2025.svg" class="opacity-100 w-[90%]"/>
</div>

<div class="relative w-full h-[150px] mouse-kde-reveal">
  <!-- Step 1 & 2: left 1/3 visible -->
  <img
    src="/mouse_kde_per_state.png"
    class="absolute inset-0 w-full h-full object-contain mouse-kde-left-third"
    v-click="[3,5]"
  />

  <!-- Step 2: right 1/3 visible (so left + right at click 8) -->
  <img
    src="/mouse_kde_per_state.png"
    class="absolute inset-0 w-full h-full object-contain mouse-kde-right-third"
    v-click="[4,5]"
  />

  <!-- Step 3: full image -->
  <img
    src="/mouse_kde_per_state.png"
    class="absolute inset-0 w-full h-full object-contain"
    v-click="5"
  />
</div>



---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# We can relate states to other behavioural measures 


:: left :: 

## Monkey 

<div v-click="2" class="flex gap-4 mt-20">
  <img src="/monkey_block_entropy_and_p_stochastic_logodds_lme_fit.svg" class="opacity-100 w-[50%]"/> 
  <img src="/monkey_mutual_info_and_p_stochastic_logodds_lme_fit.svg" class="opacity-100 w-[50%]"/>
</div>


:: right :: 
## Mouse 

<div v-click="1" class="flex gap-4 mt-20">
  <img src="/entropy_and_log_p_stochastic_lme_fit.png" class="opacity-100 w-[47%]"/> 
  <img src="/mutual_info_and_logodds_p_stochastic_lme_fit.png" class="opacity-100 w-[47%]"/>
</div>


<div v-click="1" class="absolute bottom-20 left-60 w-[45%] text-sm opacity-75">
  <hr class="border-t border-gray-600 opacity-0 mb-2" />
  
  > $P(S)$ is the probabilty of being in the stocahstic state. The log-odds $\log \left( \frac{P(S)}{1 - P(S)} \right)$ is taken here to linearize it.
</div>


<div v-click="3"
     class="absolute bottom-30 left-80 w-[35%] 
            bg-yellow-200/90 text-black text-lg font-semibold 
            p-4 rounded-xl shadow-xl leading-snug">
  Overall, unsupervised clustering of left/right choices via GLM-HMM captures changes in  higher-order statistics of behaviour (entropy, mutual info, WSLS)
</div>


---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# Are monkeys better at the task than mice?

<div class="flex w-full mt-10 gap-8">
  <!-- LEFT: 2×2 grid that gets replaced in-place -->
  <div class="w-1/2 relative">
    <!-- 2×2 grid, shown until click 5 -->
    <div class="grid grid-cols-2 gap-4" v-click-hide="5">
      <img v-click="1" src="/monkey_p_stochastic_heatmap.svg" class="w-full" />
      <img v-click="2" src="/mouse_p_stochastic_heatmap.svg" class="w-full" />
      <img v-click="3" src="/mean_p_stochastic_per_trial_and_session_interpolated_monkey.svg" class="w-full" />
      <img v-click="4" src="/mean_p_stochastic_per_trial_and_session_interpolated_mice.svg" class="w-full" />
    </div>

  <!-- Replacement image, same position, appears on click 5 -->
  <div v-click="5" class="absolute inset-0 flex items-center justify-center">
    <img src="/mouse_monkey_inverted_U_shape_p_stochastic.svg"
          class="w-full h-full object-contain" />
  </div>
</div>

  <!-- RIGHT: 2×2 grid -->
  <div class="grid grid-cols-2 gap-4 w-1/2">
    <img v-click="7" src="/mouse_and_monkey_segment_length_and_entropy.svg" class="w-full" />
    <img v-click="8" src="/mouse_and_monkey_entropy_vs_reward_rate_segment_length_300.svg" class="w-full" />
    <img v-click="9" src="/mouse_and_monkey_reward_and_entropy_as_func_of_seg_length.svg" class="w-full" />
    <!-- Optional: use v-click="9" if you want an extra step -->
    <div></div>
  </div>
</div>

<div v-click="6"
     class="absolute bottom-0 left-30 w-[35%] 
            bg-yellow-200/90 text-black text-lg font-semibold 
            p-4 rounded-xl shadow-xl leading-snug">
  Overall, monkeys can sustain stochastic states better. But how about if we focus on stochastic sequences? 
</div>

<div v-click="10"
     class="absolute bottom-30 left-170 w-[28%] 
            bg-yellow-200/90 text-black text-lg font-semibold 
            p-4 rounded-xl shadow-xl leading-snug">
  Higher entropy in monkeys 
  Similar reward rates
</div>



---
transition: fade-out 
layout: default
---

# Interim summary 

<div class="mt-30">

<v-clicks>

1. In the monkey dataset, GLM-HMM can recover behavioural strategies and their changes as monkeys adapt to different computer opponents 
2. Both monkeys and mice learn to increase their choice randomness, characterised by a "stochastic state"
3. There is some evidence to suggest that monkeys may be more random in these stochastic states and can sustain theses stochastic states for longer

</v-clicks>

</div>

---
transition: fade-out 
layout: default
---


# Mouse vs mouse matching pennies


<div class="flex flex-col items-center gap-0 mt-0">

  <!-- First row, appears on first click -->
  <div v-click="1" class="flex justify-center gap-8 w-[85%]">
    <img src="/mouse_vs_computer_cartoon_diagonal.png" class="opacity-100 w-[40%]"/>
    <img src="/computer_opponent_choice_sequences.png" class="opacity-100 w-[60%]"/>
  </div>

  <!-- Second row, appears on second click -->
  <div v-click="2" class="flex justify-center gap-8 w-[85%]">
    <img src="/mouse_vs_mouse_cartoon_diagonal.png" class="opacity-100 w-[40%]"/>
    <img src="/mouse_opponent_choice_sequences.png" class="opacity-100 w-[60%]"/>
  </div>

</div>


---
transition: fade-out 
layout: default
---


# Mouse vs mouse matching pennies : example game


<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const video = document.getElementById('myvideo')
  if (!video) return

  // Hide controls initially
  video.controls = false

  // When user clicks the video, start playing
  video.addEventListener('click', () => {
    video.play()
  })

  // When it ends: pause, show the last frame, hide controls
  video.addEventListener('ended', () => {
    video.pause()
    video.currentTime = video.duration
    video.controls = false
  })
})
</script>

<div class="flex items-center justify-center gap-2 pt-20"> 
  <img src="/mouse_vs_mouse_cartoon.png" class="opacity-100 w-[20%]"/> 

  <video
id="myvideo"
src="/animation.mp4"
controls
preload="auto"
class="w-[120%]"
onloadedmetadata="this.playbackRate = 2;"
/>

</div>


---
transition: fade-out 
layout: default
---

# Randomness and rewards when playing against computer vs. mice 

<img src="/JOA-M-0029_reward_and_entropy_during_solo_vs_social.png" class="opacity-100 w-[75%]"/>

<img src="/JOA-M-0033_reward_and_entropy_during_solo_vs_social.png" class="opacity-100 w-[75%]"/>


<div v-click class="absolute top-[60%] left-180 w-[40%] -translate-y-1/2">
  <img src="/entropy_reward_correlation.png" class="opacity-100 w-[60%]"/>
</div>


---
transition: fade-out 
layout: default
---

# Summary 

<div class="mt-30">

<v-clicks>

1. Both monkeys and mice learn to play matching pennies against a computer opponent 
2. Monkeys show longer sequences with higher entropy, but have similar reward rates to mice
3. We are now working on multiplayer matching pennies to look at adaptation to opponent's change in strategy

</v-clicks>

</div>