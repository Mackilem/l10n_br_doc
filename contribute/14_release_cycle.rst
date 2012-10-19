
.. _release_cycle:

OpenERP Release Policy FAQ
--------------------------

OpenERP is available in two different series: the *Stable* series (5.0, 6.0, 6.1, ...), suitable for production deployment, and the *Trunk* series, which is the under-development version to prepare the next stable series.
The stable series are initially in maintenance stage, which indicates that they receive no further improvement or features, but only bug corrections.
Conversely, the trunk series is where all the new features and improvements are being introduced, and therefore it is usually not suitable for production deployment.

Here is a list of the most common questions we get about the release policy.

1. When are new stable/major versions released and how are they numbered?

The frequency of major stable releases has fluctuated in the past, but the current policy is to release a new stable version every 6 months on average, with one out of three stable versions being a Long Term Support (LTS) version. An LTS version is normal stable version, but one that is supported for an extended time under the OpenERP Publisher's Warranty (OPW).
Stable versions are labelled as a decimal number with 2 components (e.g. 6.1), where the leftmost part indicates the corresponding Long Term Support (LTS) version, and the second digit indicates successive stable releases between two LTS versions.

As an illustration, here is a prospective list of future releases:

  - 09/2011: 6.1 
  - 03/2012: 6.2 
  - 09/2012: 7.0 LTS
  - 03/2013: 7.1

2. How long are LTS version actually supported? And what do you mean exactly by 'supported'?

The OpenERP Publisher's Warranty contract covers the 3 last LTS version in parallel. This means that when a new LTS version is released, an older version reaches its end-of-life, and is not supported anymore.
As an example, 6.0 LTS will be supported along with 7.0 LTS and 8.0 LTS, but will reach end-of-life when 9.0 LTS is released.
The OPW contract defines the kind of support you get for each covered version. This usually includes unlimited bug fixes.
You can also read in detail our bug correction policy here: http://doc.openerp.com/v6.0/contribute/11_bug_tracker.html#bug-management-policy                  

3. What is the difference between a LTS version and another major version? Is the upgrade procedure different?

Apart from the extended support period, a LTS version is just a normal major version. Any major version introduces many new features and improvements, and some changes that may not be fully compatible with previous version. This is true for non-LTS major versions too. For each major version, you can upgrade via OPW's migration services.

4. What is the difference between a minor/patch version and a major version? Is the upgrade procedure different?

Major versions introduce new features and may not be directly compatible with previous stable series. As a result, a complete migration process has to be followed when going from one major version to the next. This is available via the OPW.
Minor versions only introduce bug corrections, but no new features, so the upgrade procedure is built-in in OpenERP Server. You simply need to restart the server once with the additional options "-d <DB> -u all".

.. hint:: See also the :ref:`installation-link` section for more details 
          regarding the update process.

5. When are minor/patch versions released? How are they numbered? Where can the release schedule be found?

Minor versions (a.k.a. patch versions) do not follow a fixed schedule, but are instead released as soon as our OPW team considers that important bugs have been corrected, or that a large number of smaller corrections are now available. If very important issues are discovered one after the other, it may be possible for several patch versions to be released quite close to each other.
Minor versions are labelled with 3 numbers (e.g. 6.1.2) where the 2 leftmost numbers correspond to the major release, and the last number indicates successive minor releases between two LTS versions. The most recent minor version (the one with the highest 3rd number) is the recommended one for all production environments.
As there is no fixed release schedule, it is not possible to publish it beforehand. The series of milestones on Launchpad are just prospective dates, and may change without notice.

6. I really need a given stable bugfix, but there is no minor version that contains it yet. What can I do?

If the bug has already been corrected in the corresponding stable series, it means that you can already download it from the source repository on Launchpad, and apply it to your installation.
If you prefer to have a full installation package, you can contact the OPW team via your usual OPW channel and explain why this bug requires a faster release.
We also plan to provide very soon a nightly build system so that the latest code for each series can always be downloaded as a full installer, without waiting for a formally tagged release.

