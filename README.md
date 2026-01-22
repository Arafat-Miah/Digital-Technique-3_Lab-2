# Digital Technique 3 – Lab 2  
## Control Unit Verification (APB + Command Interface)

**Course:** Digital Technique 3  
**Lab:** Lab 2 – Control Unit Testbench Development  
**Student:** Arafat Miah  

---

## 📌 Objective of Lab 2

The goal of Lab 2 is to develop and debug **SystemVerilog test tasks** for verifying a Control Unit using an **APB interface**, command decoding, FIFO handling, and timing-dependent control logic.  
The focus is on **verification**, not RTL design.

This lab emphasizes:
- Writing structured test tasks
- Using assertions correctly
- Debugging timing-related failures
- Verifying behavior through waveform analysis

---

## 🧩 What Was Implemented / Modified

In this lab, I **did not write the full testbench from scratch**.  
Instead, I **modified and fixed specific test tasks** provided in the lab framework so that all functional checks pass correctly.

### ✔ Key Modifications Done by Me

- **Fixed timing assumptions** in command-related tests
- Corrected **assertion placement** to match APB ACCESS phase behavior
- Updated **`req_tick_test`** to avoid over-strict cycle assumptions
- Ensured all tests are **isolated using proper reset handling**
- Resolved simulation failures caused by **state dependency between tests**

All changes were made **only inside the test task file**, without modifying the DUT RTL.

📄 **Modified code file included:**  
- `Updated code_for lab2 only.txt`

---

## 🧪 Tests Covered in Lab 2

The following verification tasks are executed successfully in RTL simulation:

- `apb_test`
- `address_decoding_test`
- `register_test`
- `fifo_bus_test`
- `prdata_off_test`
- `cmd_clr_test`
- `cmd_cfg_test`
- `cmd_level_test`
- `req_tick_test`
- `performance_test`

All tests complete **without assertion failures**.

---

## 📊 Simulation Evidence (Waveforms & Logs)

To prove correctness of my modifications, I included the following screenshots:

### 1️⃣ Full Test Execution – Waveform View  
**File:** `lab2_waveform_overview.png`  
- Shows APB signals, control outputs, FIFO activity, and audio outputs  
- Confirms correct sequencing after command execution

### 2️⃣ Simulation Transcript – All Tests Passed  
**File:** `lab2_simulation_transcript.png`  
- Confirms successful execution of all test tasks  
- No assertion failures or fatal errors

These screenshots directly demonstrate that the **modified test code works as intended**.

---

## 🧠 Learning Outcome

This lab significantly improved my understanding of:

- How **assertions** are written and why they are essential in verification
- Difference between **functional intent vs timing-safe checks**
- Debugging failures using **waveform-driven reasoning**
- How real verification engineers structure test tasks

Initially, assertions were difficult to understand.  
To overcome this, I practiced assertion writing using simple examples (e.g., half-adder behavior), then applied the same principles here.  
AI tools were used **only as guidance**; the final logic and fixes were implemented by me after understanding the root cause.

⏱ **Time invested:** ~30+ hours

---

## ⚠️ Notes

- This repository contains **only my modified verification code**, not full lab sources
- RTL design files are **not included**
- This repository is for **academic and learning showcase purposes only**

---

## ✅ Lab Status

✔ All Lab 2 verification tests **PASS**  
✔ Assertions behave as per functional specification  
✔ Timing issues resolved correctly  

---

