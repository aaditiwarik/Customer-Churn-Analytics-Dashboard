A Create Resource Group:
1 Log into Azure Portal
2 On the top search bar, type Resource groups → click on it.
3 Click + Create.
4 Fill in:
   a.Subscription → Pay-As-You-Go (or Free Trial).
   b.Resource group name → rg-customerchurn.
   c.Region → Central India (close to my location).
5 Click Review + Create → then Create.
✅ Result: New resource group rg-customerchurn created.

B. Create Storage Account

1 In Azure Portal → search Storage accounts.
2 Click + Create.
3 On the Basics tab:
  a.Subscription → same as above.
  b.Resource group → rg-customerchurn.
  c.Storage account name → customerretentiondata.
  d.Region → Central India.
  e.Performance → Standard.
  f.Redundancy → LRS (Locally redundant).
 4 Leave Advanced / Networking / Security tabs as default.
 5 Click Review + Create → then Create.

✅ Result: Storage Account customerretentiondata created.

3. Create a Container

Open the new Storage Account (customerretentiondata).

On the left-hand menu → under Data storage → click Containers.

Click + Container (top bar).

Fill in:

Name → customerchurn (must be lowercase).

Public access level → Private (default).

Leave Advanced settings unchecked (no extra encryption needed).

Click Create.

✅ Result: Container customerchurn created.

4. Upload Dataset CSV

Go inside the container customerchurn.

Click Upload.

Click Browse for files → select WA_Fn-UseC_-Telco-Customer-Churn.csv (the dataset).

Leave default settings → Click Upload.

Wait until the progress bar shows success.

✅ Result: CSV uploaded to Azure Blob Storage.

5. Verification

Inside container → confirm that Telco-Customer-Churn.csv is listed.

Check file size & last modified timestamp.

Dataset is now ready for further use (e.g., importing into MySQL).

⚠️ Errors I Faced

Unsure about order of creation → fixed after realizing:
Resource Group → Storage Account → Container → File Upload.

Confusion about Private/Public → kept Private (best practice).

Advanced settings (immutability/encryption) → left defaults.
