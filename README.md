# Nomination Form Filler: how to use it

**Open:** double-click `Nomination Form Filler.html` and it opens in Chrome or Edge. It's one file with nothing to install, and it works without internet. Customer details stay on your computer and are never uploaded anywhere. You can copy the file to your Desktop or share it with your team.

**Web link:** https://laimeitou1126.github.io/nomination-form-filler/

## Put it on your phone as an app

- **Android (Chrome):** open the web link, tap the **⋮** menu, then **Add to Home screen** (or **Install app**), then **Install**.
- **iPhone (Safari only, not Chrome):** open the web link, tap the **Share** button (the square with an arrow), then **Add to Home Screen**, then **Add**.

The **Nomination** icon appears on your home screen and opens full screen like a normal app. After the first time it opens, it also works without internet. Downloaded PDFs go to the phone's Downloads (Android) or the **Files** app (iPhone).

## Fill in one form, step by step (the easiest way)

The app opens on **Fill in a form, step by step**. It asks for the details in 5 short steps:

1. **Policy & policyowner**
2. **Nominees**: up to 4 nominees, whose shares must add up to 100%.
3. **Trustee**: optional, so skip it if none is being appointed.
4. **Witness**: usually the agent's name and IAC No.
5. **Check & download**: fix anything in red, click **Preview the filled form**, tick the box, then click **Download filled PDF**.

Each step has a short explanation at the top. Problems show up as you type, and a step that needs fixing is marked with "!". You can jump between steps by clicking the step names. Anything you leave empty stays blank on the form so it can be handwritten. **Start over** clears everything.

Nothing you type is saved. If you close the page before downloading, the browser asks you to confirm first.

## Many customers at once (bulk)

Open the **Upload files / many customers** tab.

1. Click **Download bulk upload template (.xlsx)**. The template has one row per customer, and its second sheet, "How to fill", explains each column.
2. Fill in the rows. Leave a cell empty if you don't know it; that box stays blank on the form.
3. Drop the filled Excel file onto the app. All customers appear in the **Customers** list:
   - **Ready:** passed every check. A "blank" count means some boxes will be left empty to complete by hand.
   - **To fix:** for example a wrong NRIC, an impossible date, or shares not adding up to 100%. Click **Open**, correct it on screen, and the row turns Ready.
4. Approve customers by ticking their **Approve** box, or click **Approve all without errors** after you've checked them.
5. Export:
   - **Export approved as ZIP:** one PDF per customer, named like `2000000001_CUSTOMER_NAME_nomination.pdf`. These PDFs stay fillable, so blank boxes can still be typed into.
   - **Export approved as one combined PDF:** every approved form in a single file, ready to print in one go. This one is flattened: the text is fixed and can't be edited.

Editing a customer's details removes their approval until you approve them again, so nothing changes after you've approved it.

## Upload a form that's already filled in

Drop a filled nomination form PDF onto the app, and every answer on it loads into the edit screen, so you can check it, correct it and export it again. This works with:
- forms exported from this app's ZIP or single download;
- forms filled in on screen in Acrobat or Edge.

It does **not** work with forms that have been printed and scanned, or with the **combined PDF** export: their answers are fixed into the page and can't be read back. Use the ZIP export to keep forms re-uploadable.

The form only has 2-digit birth years (e.g. "82"). These are read as 1982 or 2082, whichever isn't in the future, so check the ages look right.

## One customer from files

In the **Upload files / many customers** tab:

1. Drop in the customer's files: an ePartner "Policy Detail Information" PDF, an already-filled nomination PDF, Excel or CSV. Files for the same policy are combined. Or click **Start a blank form** and type everything in.
2. Check and complete the details on screen. The **Checks** panel updates as you type:
   - **red** must be fixed;
   - **amber** means check with the customer (e.g. "this becomes a trust policy");
   - **blue** means not provided, so that box is left blank.
3. Click **Preview filled form** to see every page. Then tick **"I have checked this form…"** and **Download filled PDF**.

## Activity log

Bottom-right panel: what was loaded, approved and exported, with the date and time. **Download** saves it as a text file. It holds no NRIC numbers and stays in this browser only.

## What stays manual

- Signatures and signing dates (policyowner, witness, trustees, consent) must be done in person.
- The customer's legal choices, such as trust policy or trustee, or nomination versus assignment. The app flags these but doesn't decide them.
- Submitting the signed forms.

## Not supported

Scanned or photographed PDFs, other PDF layouts, and old `.xls` files (save them as `.xlsx`). These are rejected with a message saying why.

## For whoever maintains it

The source is in `app/` and shares its checks with `forms/nomination/form.js`. After changing anything, rebuild with `node app/build.js`.
