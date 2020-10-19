| Issue        | #13 |
| ------------ | -- |
| author       | Günter Windsperger @01302775|
| released by  | Nicolas Griebenow @01617265 |
| release date | 2020-10-19 |


# Legal environment
For this project several different frameworks, libraries and assets are in usage. In the following, we want to examine each of their license agreements to ensure legal compliance.

| Framework, Library or Asset         | License    |
| ----------------------------------- | ---------- |
| Spring-Framework                    | Apache 2.0 |
| Angular-Framework                   | MIT |
| H2                                  | MPL 2.0 / EPL 1.0  |
| Android Open Source Project (AOSP)  | Apache 2.0 |
| Google ARCore Android SDK           | Apache 2.0 |
| Bootstrap-Library                   | MIT |
| 3D Models for AR                    | Royalty-Free / Private usage |


The table above shows that almost all used assets are licensed under the MIT or Apache 2.0 license.  
Both licenses are permissive free software licenses with a great degree of freedom in the software usage. ‘Permissive’ means that the licenses do not have a copyleft-clause, which specifies that derived software must be licensed under the same license conditions as the original software. This way, it would not be allowed to restrict the usage of a software derived from another software which is licensed with a copyleft-clause (e.g. a software under the GPL license).  
Thus, both mentioned licenses permitting almost any further usage or distribution of the software, in a private or commercial way. Even relicensing the free software as proprietary is permitted.   
The only requirement is the preservation of copyright and license notices.  

As database engine we will use H2, which is dual licensed under the MPL and EPL. This means, that one license can be chosen freely. Both licenses are similar and are considered as weak copyleft-licenses. This means that the licensed code part need to remain under the original license but still can be used together with proprietary code. That way, those licenses are kind of a compromise between the permissive MIT/Apache (or BSD) licenses and the stronger GPL-License, which has a strong copyleft-clause.

Furthermore, we need some 3D models for the AR-part of the mobile application. We could identify an [artist](https://free3d.com/de/user/printable_models) on the website [free3d](https://free3d.com) that provides free models of different animals.
The assets provided by the website are generally licensed under the royalty-free-license, under which a broad license for the assets can usually be acquired for a one-time fee. However, this use can be further restricted by the creator. In our case, the found models are free and licensed for private usage. Unfortunately, there are no further details about the license conditions. However, permitted use should include LVA-internal proof-of-work and demonstrations.  

_Terms of Use - Google ARCore Android SDK_  
Google’s ARCore uses the Google Play Services. Therefore, it is necessary to enclose the usage and how it collects and processes data to potential end users. As mentioned in their github-repository, this could be done by incorporating the following text on the main screen or an notice dialog "This application runs on [Google Play Services for AR (ARCore)](https://play.google.com/store/apps/details?id=com.google.ar.core), which is provided by Google LLC and governed by the [Google Privacy Policy](https://policies.google.com/privacy)".

Weblinks with details to above mentioned licenses:
- [MIT License](https://opensource.org/licenses/mit-license.php)  
- [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0)  
- [Eclipse Public License 1.0](https://opensource.org/licenses/eclipse-1.0.php)  
- [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/)  
- [Royalty Free License](https://free3d.com/royalty-free-license)  
