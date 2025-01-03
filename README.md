# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications involving the `useEffect` hook and `setInterval`.  The example shows how forgetting to return a cleanup function from `useEffect` when using `setInterval` leads to a memory leak and unexpected behavior. The solution showcases the correct implementation with a cleanup function to prevent these issues.

## Problem

The `setInterval` function keeps running indefinitely without a way to stop it. Once the component unmounts, the interval continues to run, causing a memory leak. This can lead to performance issues or even crashes in your application.

## Solution

The solution involves returning a cleanup function from `useEffect`. This function clears the interval using `clearInterval` when the component unmounts, preventing the memory leak. 