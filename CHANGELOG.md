
# Development

* wget -qO - https://github.com/Arni/ding_loan/commit/b074e104798fe8d914e38860b0ce17aca792d107.diff | patch p1 -> https://itkdev.atlassian.net/browse/AAKBET-250 
* wget -qO - wget -qO - https://patch-diff.githubusercontent.com/raw/ding2/ding2/pull/250.diff | patch -p1 -> https://itkdev.atlassian.net/browse/AAKBET-251
* https://github.com/vejlebib/vejlebib_fbs

# 2.5.1

* Added update functions to remove old "mobil app" flags from the database.
* Updated openings hours panels plugins to only display "links" for opening hours that have content.


# Previous releases

This is changes in relation to DDB CMS (core) before this change log was started.

## Ding WAYF implementation
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/alma-wayf.diff
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/ddbasic-wayf.diff
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_frontend-wayf.diff
* http://github.com/aakbcms/ding_wayf_dk.git

__Note__: AAKB uses "WAYF" directly and not DBC's gate-wayf.

## Opening hours
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/ddbasic-opening-hours.diff'
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_library-opening-hours.diff
* https://www.drupal.org/files/issues/opening_hours-view_modes-2607314-6.patch


## Different permission changes:
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_perm-override-node.diff
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_perm-adv-user.diff
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_perm-aakb-survey.diff

## Aakb survery
* https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_user_frontend-aakb_survey.diff
* http://github.com/aakbcms/aakb_survey.git

## Other changes
* Ding user provider access: https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_reservation-messages.diff
* Display better reservation messages: https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_user_access.diff
* Ezproxy: git@github.com:aakbcms/ting_ezproxy.git
* App feeds (ding_redia_rss): http://github.com/aakbcms/ding_redia_rss.git (feature/aakb-patched)
* Remove un-used webtrends plugins: https://github.com/ding2/ding2/compare/master...aakbcms:feature/ding_webtrends-unused-plugin.diff
* Fix to alma block codes (AAKBET-98): https://github.com/ding2/ding2/compare/master...aakbcms:feature/alma-blockcode.diff
* Place2book (sale-not-started): https://github.com/ding2/ding2/compare/master...aakbcms:feature/ddbasic-place2book.diff


## Contribute modules:
* imagemagick
* override_node_options
* advuser
