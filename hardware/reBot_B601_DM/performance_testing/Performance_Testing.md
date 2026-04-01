# 🧪 reBot-DevArm Physical Performance Testing Reference

<p align="center">
  <img src="./images/v1.0.png" alt="reBot-DevArm Banner">
</p>

<p align="center">
  <strong>
    <a href="./Performance_Testing_zh.md">简体中文</a> &nbsp;|&nbsp;
    <a href="./Performance_Testing.md">English</a> &nbsp;|&nbsp;
    <a href="./Performance_Testing_JP.md">日本語</a>&nbsp;|&nbsp;
    <a href="./Performance_Testing_Fr.md">français</a>&nbsp;|&nbsp;
    <a href="./Performance_Testing_es.md">Español</a>
  </strong>
</p>

> [!NOTE]
> This document provides performance testing data reference for the reBot Arm B601-DM under normal and extreme working conditions.

> [!WARNING]
> **Version Difference Notice**: This test is based on the reBot Arm B601-DM equipped with **Damiao V4 version motors**. **V3 and earlier motor versions have performance differences**. Test data is for reference only; actual performance should be verified through testing.

---

## 💡 Quick Summary

**Test Termination Reason**: All tests were terminated due to **Motor 2 (upper arm joint) overheat protection**, not mechanical structural failure.

**Dynamic Motion Test** (Single motion cycle: 5s standard, reciprocating motion):

| Reach Range | Load | Duration | Termination Reason |
|----------|------|----------|----------|
| 5%~70% Rated Reach | 1.5 kg | > 2 h | Motor 2 temperature reached 90℃ |
| 5%~70% Rated Reach | 2.5 kg | 40 min | Motor 2 overheat protection |
| 5%~100% Rated Reach | 1.5 kg | 45 min | Motor 2 overheat protection |

**Static Holding Test**:

| Reach Position | Load | Duration | Termination Reason |
|----------|------|----------|----------|
| 70% Rated Reach | 1.5 kg | 18 min | Motor 2 overheat protection |
| 100% Rated Reach | 1.5 kg | 3 min | Motor 2 overheat protection |

> 👉 **Key Conclusion**: The manipulator structural strength is sufficient. Test termination was due to **Motor 2 overheat protection**. Recommended working load is **1.5 kg or less**, working reach is recommended to be **less than 70%**, and adding active cooling measures is advised.

---

## 📋 Table of Contents

- [⚡ Extreme Working Performance Test](#-extreme-working-performance-test)
- [📈 Official Load Curve](#-official-load-curve)
- [📝 Test Conclusions and Recommendations](#-test-conclusions-and-recommendations)
- [🙋 Frequently Asked Questions (FAQ)](#-frequently-asked-questions-faq)
- [📅 Update History](#-update-history)
- [📞 Technical Support](#-technical-support)

---

## ⚡ Extreme Working Performance Test

### Test Conditions

**Dynamic Motion Test**:
- Single motion cycle duration: 5 s
- Motion mode: Reciprocating motion
- Test reach range: 5%~70% / 5%~100% rated reach

**Static Holding Test**:
- Test posture: Static posture with load holding
- Test reach: 70% / 100% rated reach

### Test Results

#### 1. Dynamic Motion Test

| Test Position | Load (kg) | Max Duration | Termination Reason |
|----------|-----------|--------------|----------|
| Reach 5%~70% | 1.5 | > 2 h | Motor 2 overheat protection |
| Reach 5%~70% | 2.5 | 40 min | Motor 2 overheat protection |
| Reach 5%~100% | 1.5 | 45 min | Motor 2 overheat protection |

#### 2. Static Holding Test

| Test Position | Load (kg) | Max Duration | Termination Reason |
|----------|-----------|--------------|----------|
| Reach 70% | 1.5 | 18 min | Motor 2 overheat protection |
| Reach 100% | 1.5 | 3 min | Motor 2 overheat protection |

---

## 📈 Official Load Curve

![12Nm Load Curve](./images/12Nm.png)

<p align="center">Damiao 43 Series Motor 12Nm Version Load Curve</p>

---

## 📝 Test Conclusions and Recommendations

### Usage Recommendations

1. **Recommended Working Conditions**
   - Load: < 1.5 kg
   - Working radius: < 70% reach (450 mm)
   - Motion speed: < 70% maximum speed
   - Ambient temperature: 15 °C ~ 35 °C

2. **Cooling Recommendations**
   - When working under high load for extended periods, adding active cooling is recommended
   - After 2 hours of continuous work, a 10~15 minute rest is recommended
   - Avoid direct sunlight and use in enclosed spaces

---

## 🙋 Frequently Asked Questions (FAQ)

<details>
<summary><b>Q1: Will the manipulator's performance decrease in high-temperature environments?</b></summary>

Yes. When the ambient temperature exceeds 35 °C or the motor temperature exceeds 75 °C, it is recommended to reduce load and motion speed to ensure accuracy and lifespan. Continuous use in high temperatures is not recommended.

</details>

<details>
<summary><b>Q2: Is the test data applicable to all versions?</b></summary>

This test is based on the reBot Arm B601-DM equipped with **Damiao V4 version motors**. **V3 and earlier motor versions have performance differences**, so test data is for reference only.

</details>

---

## 📅 Update History

| Version | Date | Update Content | Author |
|------|------|----------|------|
| v1.0 | 2026.04.01 | Initial version, releasing basic performance test data | SeeedStudio AI Robotics Team |

---

## 📞 Technical Support

If you have any questions related to performance testing, please feel free to contact us:

- **Technical Support**: yaohui.zhu@seeed.cc
- **Discord**: [Join Community](https://discord.gg/AbGuqJhDpQ)
- **Wiki**: [View Knowledge Base](https://wiki.seeedstudio.com/robotics_page/)

---

<p align="center">
  <strong>🤖 reBot-DevArm - Open Source Manipulator for Every Developer</strong>
</p>
