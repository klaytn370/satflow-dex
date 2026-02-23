# SatFlow DEX Architecture

## Overview

SatFlow DEX is a minimal Automated Market Maker (AMM) built on OP_NET (Bitcoin Layer 1).
It implements a two-token liquidity pool using the constant product formula:

    reserveA * reserveB = k

    The goal of this project is to demonstrate a simple, understandable DeFi primitive
    that can run on Bitcoin L1 via OP_NET.

    ---

    ## Components

    ### SatFlowPool Contract

    Main contract: `contracts/SatFlowPool.opnet`

    Responsibilities:
    - Hold reserves of TokenA and TokenB (OP20 tokens)
    - Track liquidity provider (LP) shares
    - Handle:
      - Adding liquidity
        - Removing liquidity
          - Swaps between TokenA and TokenB

          ---

          ## Core Mechanics

          - Users deposit two tokens and receive LP shares
          - Swaps follow the formula: x * y = k
          - A small fee is applied to swaps
          - LP shares represent proportional ownership of the pool

          ---

          ## Design Goals

          - Minimal and easy to understand
          - Hackathon-friendly
future