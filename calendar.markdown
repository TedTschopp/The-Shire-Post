---
layout: page
title: Calendar Reckoning
permalink: /calendar/
nav: calendar
---

<div class="eyebrow">public notice</div>
<h1 class="notice-title">Calendar Reckoning at the Counter</h1>
<div class="rule-short"></div>

<style>
/* Old Man Eloquent loaded via site.css */

.postmaster-ledger {
  font-family: 'Old Man Eloquent', cursive;
  letter-spacing: 0.01em;
}

.postmaster-ledger li,
.postmaster-ledger p,
.postmaster-ledger h2,
.postmaster-ledger h3 {
  font-family: 'Old Man Eloquent', cursive;
}

.postmaster-ledger table,
.postmaster-ledger th,
.postmaster-ledger td {
  font-family: 'Dana Library Hand', monospace;
}
</style>

<p class="lede">
  This office keeps records in the Shire Reckoning and accepts appointments from
  neighbors who use the Common (Gregorian) calendar.
</p>

<section class="notice" style="margin-top: 22px;">
  <h3>Today, in both calendars</h3>
  <table class="ledger">
    <thead>
      <tr>
        <th scope="col">Common calendar</th>
        <th scope="col">Shire calendar</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>{{ "now" | date: "%A, %-d %B %Y" }}</td>
        <td>{% include shire-date-full.html %}</td>
      </tr>
    </tbody>
  </table>
</section>

<section class="notice" style="margin-top: 22px;">
  <h3>Month names and special days</h3>
  <p>
    The Shire year has twelve thirty-day months, plus festival days that do not
    belong to any month.
  </p>
  <table class="ledger">
    <thead>
      <tr>
        <th scope="col">Common (approx.)</th>
        <th scope="col">Shire reckoning</th>
        <th scope="col">Notes for local use</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>Jan</td><td>Afteryule</td><td>Begins after 2 Yule</td></tr>
      <tr><td>Feb</td><td>Solmath</td><td>Winter bookkeeping month</td></tr>
      <tr><td>Mar</td><td>Rethe</td><td>Spring posting lanes reopen</td></tr>
      <tr><td>Apr</td><td>Astron</td><td>Field routes stabilize</td></tr>
      <tr><td>May</td><td>Thrimidge</td><td>Current office volume rises</td></tr>
      <tr><td>Jun</td><td>Forelithe</td><td>Month ends before Lithe days</td></tr>
      <tr><td>Late Jun / early Jul</td><td>1 Lithe, Midyear's Day, Overlithe (leap years), 2 Lithe</td><td>Festival days; no month name</td></tr>
      <tr><td>Jul</td><td>Afterlithe</td><td>Resumes monthly count</td></tr>
      <tr><td>Aug</td><td>Wedmath</td><td>Harvest dispatches begin</td></tr>
      <tr><td>Sep</td><td>Halimath</td><td>Heavy parcel season starts</td></tr>
      <tr><td>Oct</td><td>Winterfilth</td><td>Route weather watch begins</td></tr>
      <tr><td>Nov</td><td>Blotmath</td><td>Early dusk affects final dispatch</td></tr>
      <tr><td>Dec</td><td>Foreyule</td><td>Year closes before 1 Yule</td></tr>
      <tr><td>Year-end</td><td>1 Yule, 2 Yule</td><td>Festival boundary days</td></tr>
    </tbody>
  </table>
</section>

<section class="notice" style="margin-top: 22px;">
  <h3>Weekdays used by the Post</h3>
  <table class="ledger">
    <thead>
      <tr>
        <th scope="col">Common name</th>
        <th scope="col">Shire name</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>Saturday</td><td>Sterday</td></tr>
      <tr><td>Sunday</td><td>Sunday</td></tr>
      <tr><td>Monday</td><td>Monday</td></tr>
      <tr><td>Tuesday</td><td>Trewsday</td></tr>
      <tr><td>Wednesday</td><td>Hevensday</td></tr>
      <tr><td>Thursday</td><td>Mersday</td></tr>
      <tr><td>Friday</td><td>Highday</td></tr>
    </tbody>
  </table>
</section>

<section class="notice" style="margin-top: 22px;">
  <h3>Desk conversion widget</h3>
  <p>
    Choose any Common date and the counter will render the equivalent Shire date
    used on slips, notices, and ledger entries.
  </p>

  <div class="field" style="max-width: 420px; margin-top: 10px;">
    <label for="common-date-input">Common calendar date</label>
    <input id="common-date-input" type="date" aria-describedby="conversion-help">
    <span id="conversion-help" class="hint">If no date is chosen, today's date is used.</span>
  </div>

  <table class="ledger">
    <thead>
      <tr>
        <th scope="col">Rendered field</th>
        <th scope="col">Value</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Common date</td>
        <td id="common-rendered">-</td>
      </tr>
      <tr>
        <td>Shire full style</td>
        <td id="shire-full-rendered">-</td>
      </tr>
      <tr>
        <td>Shire short style</td>
        <td id="shire-short-rendered">-</td>
      </tr>
      <tr>
        <td>Clerk note</td>
        <td id="shire-note-rendered">-</td>
      </tr>
    </tbody>
  </table>

  <noscript>
    <p class="hint" style="margin-top: 10px;">The conversion widget requires JavaScript. The static tables above remain valid for manual conversion.</p>
  </noscript>
</section>

<section class="notice" style="margin-top: 22px;">
  <h3>Notes for humans using the common calendar</h3>
  <ul>
    <li>Bring appointments in Common dates if that is what you use; the clerk will convert at the desk.</li>
    <li>If your letter says Highday, treat it as Friday for travel and scheduling.</li>
    <li>During Lithe days and Yule days, expect date labels that are day names rather than month/day numbers.</li>
    <li>The year count shown as <strong>Imp.A.</strong> is the office age-reckoning. In this system, <strong>Imp.A. year = AD year</strong>.</li>
  </ul>
</section>

<section class="postmaster-ledger" aria-label="From The Postmaster's Ledger" markdown="1">

## From The Postmaster's Ledger

I keep these entries as my father kept them, and his father before him, from the late Fourth Age onward.  

The reckoning has been copied by hand from clerk to clerk at this counter.

One technical note for neighbors: the historical BC/AD sequence has no year zero. We therefore keep "the boundary" in story terms, but use standard historical numbering in practical conversion.

### Master chronology (postmaster's office copy)

| Age / period | Office name | Approx. real-world span | Length | Clerk's note |
| --- | --- | --- | --- | --- |
| Creation / Ainulindale | Creation before Time | Outside ordinary dating | - | Mythic, not a counting age |
| Days before Days | Shaping of Arda | c. 62,000–28,700 BC | c. 33,500 years | Before sun-counted ages |
| Years of the Trees | Age of the Trees / Starlight | c. 28,700–18,661 BC | c. 10,000 years | Before First Age rising |
| First Age | Elder Age | c. 18,661–13,760 BC | 4,902 years | War against Morgoth |
| Second Age | Numenorean Age | c. 13,759–10,319 BC | 3,441 years | Sea-kings and Downfall |
| Third Age | Age of the Rings | c. 10,318–7,298 BC | 3,021 years | Ends with Sauron's fall |
| Fourth Age | Age of Seed and Hearth | c. 7,297–4,865 BC | 2,433 years | Reconstructed later age |
| Fifth Age | Age of Cities and Kings | c. 4,864–2,433 BC | 2,432 years | Reconstructed later age |
| Sixth Age | Age of Iron, Law, and Covenant | c. 2,432–1 BC | 2,432 years | Reconstructed later age |
| Seventh Age | Imperial Age | AD 1–present | ongoing | Current age |
{: .ledger }

### Conversion rules used at this desk

| Reckoning | Conversion |
| --- | --- |
| Imperial Age | Imp.A. year = AD year |
| Sixth Age | Si.A. year n = 2433 - n BC |
| Fifth Age | Fi.A. year n = 4865 - n BC |
| Fourth Age | Fo.A. year n = 7298 - n BC |
| Third Age | T.A. year n = 10319 - n BC |
| Second Age | S.A. year n = 13760 - n BC |
{: .ledger }

So in our current ledger style:

- Imp.A. 2026 = AD 2026
- Si.A. 2432 = 1 BC
- Si.A. 2406 = 27 BC

### Why the name "Imperial Age" is kept

The name marks not merely one imperial throne, but the long imperial frame of law, calendar, church, administration, and inherited statecraft that has shaped the AD-counted world. In short: the order changed hands many times, but the grammar of empire endured.

### Clean office summary

| Age | Office name | Dates |
| --- | --- | --- |
| Creation | Creation before Time | before ordinary reckoning |
| Days before Days | Shaping of Arda | c. 62,000–28,700 BC |
| Years of the Trees | Age of Trees / Starlight | c. 28,700–14,349 BC, overlapping the First Age after c. 18,661 BC |
| First Age | Elder Age | c. 18,661–13,760 BC |
| Second Age | Numenorean Age | c. 13,759–10,319 BC |
| Third Age | Age of the Rings | c. 10,318–7,298 BC |
| Fourth Age | Age of Seed and Hearth | c. 7,297–4,865 BC |
| Fifth Age | Age of Cities and Kings | c. 4,864–2,433 BC |
| Sixth Age | Age of Iron, Law, and Covenant | c. 2,432–1 BC |
| Seventh Age | Imperial Age | AD 1–present |
{: .ledger }

Today, by this ledger:

> Imperial Age 2026  
> May 15, Imp.A. 2026

### Sources copied into the register

- [Later Ages - Tolkien Gateway](https://tolkiengateway.net/wiki/Later_Ages)
- [Chronology - Christian Era (Britannica)](https://www.britannica.com/topic/chronology/Christian)
- [Roman Empire (Britannica)](https://www.britannica.com/place/Roman-Empire)
- [Days before days - Tolkien Gateway](https://tolkiengateway.net/wiki/Days_before_days)
- [Years of the Trees - Tolkien Gateway](https://tolkiengateway.net/wiki/Years_of_the_Trees)
- [First Age - Tolkien Gateway](https://tolkiengateway.net/wiki/First_Age)
- [Third Age - Tolkien Gateway](https://tolkiengateway.net/wiki/Third_Age)
- [Neolithic Revolution (Britannica)](https://www.britannica.com/event/Neolithic-Revolution)
- [Where writing first developed (Britannica)](https://www.britannica.com/question/Where-did-writing-first-develop)
- [Egypt summary (Britannica)](https://www.britannica.com/summary/Egypt)
- [Bronze Age (Britannica)](https://www.britannica.com/event/Bronze-Age)
- [Indus civilization (Britannica)](https://www.britannica.com/topic/Indus-civilization)
- [Shang dynasty (Britannica)](https://www.britannica.com/topic/Shang-dynasty)
- [Zhou dynasty (Britannica)](https://www.britannica.com/topic/Zhou-dynasty)
- [Hellenistic Age (Britannica)](https://www.britannica.com/event/Hellenistic-Age)

</section>

<script>
(() => {
  const input = document.getElementById('common-date-input');
  const commonRendered = document.getElementById('common-rendered');
  const shireFullRendered = document.getElementById('shire-full-rendered');
  const shireShortRendered = document.getElementById('shire-short-rendered');
  const shireNoteRendered = document.getElementById('shire-note-rendered');

  if (!input || !commonRendered || !shireFullRendered || !shireShortRendered || !shireNoteRendered) {
    return;
  }

  const commonWeekdays = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
  const commonMonths = [
    'January', 'February', 'March', 'April', 'May', 'June',
    'July', 'August', 'September', 'October', 'November', 'December'
  ];
  const shireWeekdays = ['Sterday', 'Sunday', 'Monday', 'Trewsday', 'Hevensday', 'Mersday', 'Highday'];

  const isLeapYear = (year) => {
    if (year % 400 === 0) return true;
    if (year % 100 === 0) return false;
    return year % 4 === 0;
  };

  const dayOfYear = (date) => {
    const start = Date.UTC(date.getUTCFullYear(), 0, 0);
    const current = Date.UTC(date.getUTCFullYear(), date.getUTCMonth(), date.getUTCDate());
    return Math.floor((current - start) / 86400000);
  };

  const toShire = (date) => {
    const year = date.getUTCFullYear();
    const impYear = year;
    const doy = dayOfYear(date);
    const leap = isLeapYear(year);

    let month = '';
    let day = 0;
    let festival = '';

    if (doy === 1) {
      festival = '2 Yule';
    } else if (doy <= 31) {
      month = 'Afteryule';
      day = doy - 1;
    } else if (doy <= 61) {
      month = 'Solmath';
      day = doy - 31;
    } else if (doy <= 91) {
      month = 'Rethe';
      day = doy - 61;
    } else if (doy <= 121) {
      month = 'Astron';
      day = doy - 91;
    } else if (doy <= 151) {
      month = 'Thrimidge';
      day = doy - 121;
    } else if (doy <= 181) {
      month = 'Forelithe';
      day = doy - 151;
    } else if (doy === 182) {
      festival = '1 Lithe';
    } else if (doy === 183) {
      festival = "Midyear's Day";
    } else if (leap && doy === 184) {
      festival = 'Overlithe';
    } else if (leap && doy === 185) {
      festival = '2 Lithe';
    } else if (leap && doy <= 215) {
      month = 'Afterlithe';
      day = doy - 185;
    } else if (leap && doy <= 245) {
      month = 'Wedmath';
      day = doy - 215;
    } else if (leap && doy <= 275) {
      month = 'Halimath';
      day = doy - 245;
    } else if (leap && doy <= 305) {
      month = 'Winterfilth';
      day = doy - 275;
    } else if (leap && doy <= 335) {
      month = 'Blotmath';
      day = doy - 305;
    } else if (leap && doy <= 365) {
      month = 'Foreyule';
      day = doy - 335;
    } else if (leap && doy === 366) {
      festival = '1 Yule';
    } else if (doy === 184) {
      festival = '2 Lithe';
    } else if (doy <= 214) {
      month = 'Afterlithe';
      day = doy - 184;
    } else if (doy <= 244) {
      month = 'Wedmath';
      day = doy - 214;
    } else if (doy <= 274) {
      month = 'Halimath';
      day = doy - 244;
    } else if (doy <= 304) {
      month = 'Winterfilth';
      day = doy - 274;
    } else if (doy <= 334) {
      month = 'Blotmath';
      day = doy - 304;
    } else if (doy <= 364) {
      month = 'Foreyule';
      day = doy - 334;
    } else {
      festival = '1 Yule';
    }

    if (festival) {
      return {
        full: `${festival}, Imp.A. ${impYear}`,
        short: `${festival} · Imp.A. ${impYear}`,
        note: 'Festival day: use the festival name only, no weekday or month number.'
      };
    }

    const weekdayIndex = ((day - 1) % 7 + 7) % 7;
    const weekday = shireWeekdays[weekdayIndex];
    return {
      full: `${weekday}, ${day} ${month}, Imp.A. ${impYear}`,
      short: `${day} ${month} · Imp.A. ${impYear}`,
      note: 'Ledger day: use the Shire weekday and month exactly as printed.'
    };
  };

  const render = () => {
    const raw = input.value;
    const date = raw ? new Date(`${raw}T00:00:00Z`) : new Date();
    const common = `${commonWeekdays[date.getUTCDay()]}, ${date.getUTCDate()} ${commonMonths[date.getUTCMonth()]} ${date.getUTCFullYear()}`;
    const shire = toShire(date);

    commonRendered.textContent = common;
    shireFullRendered.textContent = shire.full;
    shireShortRendered.textContent = shire.short;
    shireNoteRendered.textContent = shire.note;
  };

  if (!input.value) {
    const now = new Date();
    const yyyy = now.getUTCFullYear();
    const mm = String(now.getUTCMonth() + 1).padStart(2, '0');
    const dd = String(now.getUTCDate()).padStart(2, '0');
    input.value = `${yyyy}-${mm}-${dd}`;
  }

  input.addEventListener('change', render);
  render();
})();
</script>
