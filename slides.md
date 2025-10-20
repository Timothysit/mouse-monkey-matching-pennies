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

1. Mouse and monkey matching pennies task 
2. Mouse and monkey matching pennies behaviour analysis 


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

Data from Lee 2004 - Reinforcement learning and decision making in monkeys during a competitive game.


:: right :: 

## Mouse 

<div v-click="3">

  <img src="/mouse_dataset_choose_right.png" class="opacity-100 w-[60%]"/>
</div>


---
transition: fade-out 
layout: two-cols-title 
columns: is-6
---

:: title :: 

# Clustering behaviour into states via GLM-HMM 

<img src="/GLM-HMM-cartoon_v1.svg" class="opacity-100 w-[40%]" v-click="1"/>


:: left :: 

## Monkey

<img src="/monkey_three_states_weight.svg" class="opacity-100 w-[100%]" v-click="3"/>



:: right :: 

## Mouse



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

<div v-click="1" class="absolute bottom-5 left-12 w-3/4">
  <hr class="border-t-1 border-gray-600 opacity-0 mb-2" />
  <p class="text-sm opacity-75">
    P(WSLS) calculated as $P(X_t = Y_{t-1})$ where $X_t$ and $Y_t$ are the animal's and opponents choices on trial $t$
  </p>
</div>


:: right :: 

## Mouse 

<div v-click="2">
  <img src="/entropy_and_log_p_stochastic_lme_fit.png" class="opacity-100 w-[50%]"/>
  <img src="/mutual_info_and_logodds_p_stochastic_lme_fit.png" class="opacity-100 w-[50%]"/>
</div>

TODO: Add details about calculation in footnote