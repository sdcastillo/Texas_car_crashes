---
layout: default
title: Texas car crashes
description: Austin 2021 TxDOT crash extract for a principal components analysis, with motorcycle safety in view.
samwiki: true
---

<p class="sw-level sw-level-intermediate"><span class="sw-level-idx">Level 2</span><span class="sw-level-name">Intermediate</span></p>

<section class="sw-lede" aria-labelledby="about-title">
  <div class="sw-lede-copy">
    <h2 id="about-title">Austin crashes, with motorcycles in view</h2>
    <p>This repository holds a Texas Department of Transportation crash extract for Austin. The file was pulled from CR-3 reports on 18 March 2022 and filtered to crash year 2021 and the city of Austin. TxDOT’s query count on that pull is 13,649 crashes, 27,626 units, and 33,717 persons. The download is <a href="https://github.com/sdcastillo/Texas_car_crashes/blob/main/texas_car_crashes.zip"><code>texas_car_crashes.zip</code></a>. Each data row is a person in a crash, so the same crash is repeated for every person in it. The table has 80 columns, including road class, speed limit, weather, contributing factors, vehicle body style, and injury severity.</p>
    <p>It is for people who want that Austin file in one place, with the cleaning plan already written down. Riders and safety advocates can see where motorcycles sit in a year of city crashes. Analysts who know a train-and-test split can take the next step on a wide categorical table. The notes also invite collaborators on Austin motorcycle safety, including anyone who worked near Rex, an earlier attempt at an OnStar-like system for motorcycles.</p>
    <p><strong>Difficulty: intermediate.</strong> On the SamWiki ladder this is Level 2, intermediate. The work on the file is the usual preparation before a model: drop rows that are missing the fields you need, remove outliers, collapse sparse categories, run a principal components analysis, and split what remains into training and testing sets. The extract is the part that takes care. Many cells are the literal value <code>No Data</code>, vehicle and injury fields are codes, and a crash-level question has to be asked on person-level rows. A first course in multivariate analysis is enough to start.</p>
    <p>Motorcycle rows are why the file is here. Of 33,717 person-rows, 286 are coded <code>MC - MOTORCYCLE</code>, across 272 crashes: 273 drivers of a motorcycle-type vehicle and 13 passengers. Fourteen of those rows are coded fatal and 69 are suspected serious injury. The other 33,431 rows contain 103 fatal codes and 459 suspected serious codes. Motorcycles are under one percent of the rows and a much larger share of the severe codes in this extract. That is a description of these coded rows, and it is the reason the original notes focus on rider safety in Austin. Rex, three years before those notes, tried to build the rider-side system: real-time alerts, emergency coordination, tracking, and a link to navigation. That company work has moved on. The crash file is the part that can still be studied in the open.</p>
  </div>
  <aside class="sw-find" aria-labelledby="facts-title">
    <h2 id="facts-title">On this page</h2>
    <ul>
      <li><strong>What it is</strong> A 2021 Austin CR-3 extract in <code>texas_car_crashes.zip</code>, plus the cleaning plan from the repository README.</li>
      <li><strong>Who it is for</strong> Austin safety work, motorcycle riders and advocates, and analysts who can clean a wide categorical table and run principal components analysis.</li>
      <li><strong>Difficulty: intermediate</strong> Level 2 on the SamWiki ladder. Preparation and PCA on a person-level crash file.</li>
      <li><strong>Analysis steps</strong> Remove rows with missing data, remove outliers, simplify categorical variables, run a principal components analysis, and split into training and testing sets.</li>
      <li><strong>Collaboration</strong> Road safety, motorcycle technology, and Austin community work. The original ask is kept below.</li>
    </ul>
  </aside>
</section>

## Analysis plan

These are the steps already recorded for the file:

- Remove all entries with missing data
- Remove any outliers
- Simplify categorical variables
- Run a principal components analysis
- Split the dataset into training and testing sets

## Vision: road and vehicle safety in Austin

The project goes beyond the table. The goal is to help improve road and vehicle safety in the Austin, Texas area, with a special focus on motorcycle driver safety. Motorcycle drivers face a higher risk of accidents and injuries than other vehicle types. The extract shows where those rows concentrate: contributing factors, road class, weather, and injury severity. The point of cleaning it is to name the patterns a safety effort could act on.

## Past project: Rex

Three years before these notes, the work with a startup called Rex was to create an OnStar-like system for motorcycles:

- Real-time safety alerts and communication
- Emergency response coordination
- Rider tracking and assistance
- Integration with existing motorcycle navigation systems

That project has evolved. The mission in these notes is the same one: rider safety, studied from the crash file and open to collaborators.

## Looking for collaborators

Collaborators and partners are welcome. The original notes name four ways in:

- Road safety innovation
- Motorcycle safety technology
- Data-driven transportation solutions
- Austin and Texas community initiatives

Data scientists, software engineers, motorcycle riders, and safety advocates all have a piece of that. A change to the cleaning steps, a clearer note on the codes, or a result from the principal components analysis can come back as a pull request.

<section class="sw-contribute" aria-labelledby="contribute-title">
  <h2 id="contribute-title">Contribute</h2>
  <p>Fork <a href="https://github.com/sdcastillo/Texas_car_crashes">sdcastillo/Texas_car_crashes</a>, make the improvement, and send it back. That is how you join the work on this file.</p>
  <p class="sw-actions">
    <a class="sw-btn sw-btn-pr" href="https://github.com/sdcastillo/Texas_car_crashes/compare" target="_blank" rel="noopener noreferrer">Contribute / Open a PR</a>
  </p>
</section>
