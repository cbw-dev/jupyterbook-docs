# **Recurring Workshop**: Copying [RC]

Certain aspects of the setup for workshops will be different depending on your role. Headers ending in "[RC]" are for Regional Coordinators. Headers without "[RC]" are assumed to be relevant to both RC and workshop teams.

```{note}
You should be on this page if CBW already has a version of this workshop as a website, and you mainly wanted to reuse it (maybe with some edits).
```

## WE NEED TO TEST THIS SINCE IT USES GHP PAGES


## Recreate the Workshop

We will be creating a copy the existing workshop and workshop website by git forking the repository that hosts the existing workshop website. (This is explained more thoroughly as you actually create your website!)

**How to Git Fork**

1. **Go to the pre-existing workshop repository** under the <a href="https://github.com/bioinformaticsdotca/" target="_blank">bioinformaticsdotca GitHub</a> for the workshop you want to recreate. For example, if we wanted to create a new workshop version of <a href="https://github.com/bioinformaticsdotca/AUR_2024" target="_blank">Analysis Using R 2024 (AUR 2024)</a>, we would go to this page:
   
   <img src="https://docs.google.com/drawings/d/e/2PACX-1vR6kuw0wnLD1WL01iuZfnP3rPrDVhB-oClsjUribaDS7GpJNXw9QXbUVZ3aBCIO5N4pBKJXGtwpScfV/pub?w=2068&amp;h=597" alt="Analysis Using R 2024 GitHub Repo Screenshot">

<br>

2. **Click "Fork"** as shown below.
     <img src="https://docs.google.com/drawings/d/e/2PACX-1vQKy0kL2lRkDMug28L6zdgEw_WmUIDGhUi5vor_N5SpLyUMFvtSwTnoHpmefZChkSbEQhEcYHHNFy2Z/pub?w=2867&amp;h=997" alt="Where to find the fork button on a GitHub Repo">

<br>

3. You will be brought to this page. You need to **update** the following parts: the **owner** (change to bioinformaticsdotca, as shown), the **new repository name** (follow CBW Guidelines) and the **description**. The fork will automatically have "Copy the `main` branch only", which it should be (do not deselect this). Then, click the green `fork` button in the bottom right, as highlighted below.

    <img src="https://docs.google.com/drawings/d/e/2PACX-1vQGQ5pL3qc29i5p5m_aQmyH4YOFUCMVvfryHx3kpR8d-AviF0BKDdCd40GJSM4qc8N2P42TNMp2UIkD/pub?w=2864&amp;h=1624" alt="fork page, with edits highlighted">

<br>

4. You will be brought to your new repository, which will host the updated version of the pre-existing workshop!

Now it's time to generate a website from your newly forked repository! That is, deploy your website. Click [here](deploy)!

## Making Updates

Follow the **Editing Your Workshop** section to figure out how to start editing your workshop. However, since it is a recurring workshop, you may not need to edit much.

If you are only editing the name, date and other small details <!-- there is a word for this I can't think of right now -->, consider only editing the config.yml.