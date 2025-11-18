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


# Monkey and mouse matching pennies

Timothy Sit



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

# Behaviour 

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

<div v-click="3">

  <img src="/mouse_dataset_choose_right.png" class="opacity-100 w-[60%]"/>
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

<img src="/p_state_4_states.svg" class="opacity-100 w-[100%]" v-click="2"/>

<img src="/recovered_glm_weights_4_states.svg" class="opacity-100 w-[100%]" v-click="3"/>




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

<img src="/monkey_three_states_weight.svg" class="opacity-100 w-[100%]" v-click="3"/>



:: right :: 

## Mouse

<img src="/glmhmm_CV_delta_test_ll.svg" class="opacity-100 w-[50%]" v-click="1"/>


<img src="/clustered_glm_weights_cosyneabstract2025.svg" class="opacity-100 w-[100%]" v-click="2"/>



---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# GLM-HMM states over sessions

:: left :: 


## Monkey


<img src="/C_state_probabilities_per_session.png" class="opacity-100 w-[100%]" v-click="3"/>

<img src="/E_state_probabilities_per_session.png" class="opacity-100 w-[100%] -mt-5" v-click="4"/>

<img src="/F_state_probabilities_per_session.png" class="opacity-100 w-[100%] -mt-5" v-click="5"/>


:: right ::


<div v-click="2">
  <img src="/monkey_three_states_weight.png" class="opacity-100 w-[100%]"/>
</div>



## Mouse


<div v-click="1" class="absolute top-[70%] left-120 w-[70%] -translate-y-1/2">
  <img src="/average_pstate_smooth_cosyneabstract2025.svg" class="opacity-100 w-[50%]"/>
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
  <img src="/monkey_kde_per_state.png" class="opacity-100 w-[100%]"/>
</div>

<div v-click="1" class="absolute bottom-5 left-12 w-[45%] text-sm opacity-75">
  <hr class="border-t border-gray-600 opacity-0 mb-2" />
  
  > P(WSLS) calculated as $P(X_t = Y_{t-1})$ where <br> $X_t$ and $Y_t$ are the animal’s and opponent’s choices on trial $t$.
</div>

:: right :: 

## Mouse 

<div v-click="2">
  <img src="/clustered_glm_weights_cosyneabstract2025.svg" class="opacity-100 w-[90%]"/>
  <img src="/mouse_kde_per_state.svg" class="opacity-100 w-[100%]"/>
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


---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# Are monkeys better at the task than mice?


<div class="flex gap-4 mt-20">
  <img src="/monkey_p_stochastic_heatmap.svg" class="opacity-100 w-[25%]"/> 
  <img src="/mouse_p_stochastic_heatmap.svg" class="opacity-100 w-[25%]"/>
  <img src="/mouse_and_monkey_segment_length_and_entropy.svg" class="opacity-100 w-[25%]"/>
  <img src="/public/mouse_and_monkey_entropy_vs_reward_rate_segment_length_300.svg" class="opacity-100 w-[25%]"/>

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

