# How to Bulk Import Devices in Milesight Embedded Network Server

Milesight LoRaWAN Gateway supports downloading a template and importing multiple devices conveniently.

This article describes how to bulk import devices in Milesight Embedded Network Server. If you need to add a single device, please refer to [How to Connect LoRaWAN Nodes to Milesight Gateway](http://support.milesight-iot.com/en/support/solutions/articles/73000514280).

---

## Requirement

- Milesight LoRaWAN Gateway
- LoRaWAN end-devices

---

## Configuration

### Step 1 — Ensure Applications and Profiles Exist

Make sure there is at least 1 application and profile on **Network Server > Applications** and **Network Server > Profiles**. Please refer to [How to Connect LoRaWAN Nodes to Milesight Gateway](http://support.milesight-iot.com/en/support/solutions/articles/73000514280).

In this article, we use **cloud** in the application, and **ClassA-OTAA** in the profile.

### Step 2 — Download the Bulk Import Template

Go to **Network Server > Device**, click **Bulk Import** and download the template.

### Step 3 — Fill in the CSV Template

Fill in the device information in `template.csv`. Required attributes:

- If **Join Type** is **OTAA**:
  - `name`, `description`, `deveui`, `deviceprofile`, `application`, `payloadcodec`, `fport`, `appkey`, `timeout`, `isdefaultabp` (leave `FALSE`)

- If **Join Type** is **ABP**:
  - `name`, `description`, `deveui`, `deviceprofile`, `application`, `payloadcodec`, `fport`, `timeout`, `isdefaultabp`
  - If `isdefaultabp` is `TRUE`, you do not need to fill in `devaddr`, `appskey`, and `nwkskey`.
  - If `isdefaultabp` is `FALSE`, you need to fill in `devaddr`, `appskey`, and `nwkskey`.

### Step 4 — Example: WT201

Take WT201 as an example and fill in the corresponding fields.

### Step 5 — Import the CSV File

Click **Browse** to locate the `.csv` file and import it.

### Step 6 — Verify Import

After the bulk import is done successfully, you will see all the sensors that you filled in the `.CSV` file.

---

**--END--**
