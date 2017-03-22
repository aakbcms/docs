
# Development

# 3.0.2

## Patches:

### Du kan først forny dine lån 7 dage før de udløber, og højst to gange i alt
	* wget -qO - https://github.com/Arni/ding_loan/commit/b074e104798fe8d914e38860b0ce17aca792d107.diff | patch p1 -> https://itkdev.atlassian.net/browse/AAKBET-250

### FBS - Ingen opstilling med DK-5 signatur eller inverteret forfatternavn
	* wget https://patch-diff.githubusercontent.com/raw/ding2/ding2/pull/552.patch && git apply 552.patch
	* wget https://patch-diff.githubusercontent.com/raw/ding2/ding2/pull/21.patch && git apply 21.patch

### Filtrering på branch, availability, holdings
	* wget -qO - https://github.com/ding2/ding2/compare/7.x-3.0.2...aakbcms:feature/fbs-hackes.diff | patch -p1

### FBS - alle manifestationer på tværs af agencies vises i værkvisningen på trods af holdingsItem.agency
	* ting client ->>>> wget -qO - https://github.com/ding2/ting-client/compare/master...aakbcms:feature/holdingitems.diff | patch -p1
	* wget -qO - https://github.com/ding2/ding2/compare/7.x-3.0.2...aakbcms:feature/holdingitems.diff | patch -p1

### Fjernlån. Lånserstatus - titlen kan ikke vises testet og godkendt (Lene) - http://platform.dandigbib.org/issues/1270
	* wget https://patch-diff.githubusercontent.com/raw/ding2/ding2/pull/352.patch && git apply 352.patch

### Handle exclude branch in search
	* wget -qO - https://raw.githubusercontent.com/aakbcms/docs/master/ting-client.diff | patch -p1

## Manual changes:

### Frontpage panels
```
>               'new-9e020af4-9b1a-4a09-aae4-6e5614313c53' => array(
>                 'pid' => 'new-9e020af4-9b1a-4a09-aae4-6e5614313c53',
>                 'panel' => 'tertiary',
>                 'type' => 'node',
>                 'subtype' => 'node',
>                 'shown' => TRUE,
>                 'access' => array(),
>                 'configuration' => array(
>                   'nid' => 12361,
>                   'links' => 1,
>                   'leave_node_title' => 0,
>                   'identifier' => '',
>                   'build_mode' => 'teaser',
>                   'link_node_title' => 0,
>                   'override_title' => 0,
>                   'override_title_text' => '',
>                   'override_title_heading' => 'h2',
>                 ),
>                 'cache' => array(),
>                 'style' => array(
>                   'settings' => NULL,
>                 ),
>                 'css' => array(
>                   'css_id' => '',
>                   'css_class' => 'important-news',
>                 ),
>                 'extras' => array(),
>                 'position' => 0,
>                 'locks' => array(),
>                 'uuid' => '9e020af4-9b1a-4a09-aae4-6e5614313c53',
                ),
```

### Style changes
```
.front .tertiary-content .important-news,
.front .tertiary-content .important-news .pane-title {
  margin-bottom: 10px;
}

.front .tertiary-content .important-news .pane-content {
  background-color: #fff7b5;
}

.front .tertiary-content .important-news .page-lead {
  font-family: SourceSansProRegular;
  padding: 10px;
}

.front .tertiary-content .important-news .node-readmore {
  text-align: right;
  padding-right: 10px;
  padding-bottom: 10px;
}

.front .tertiary-content .important-news .page-title,
.front .tertiary-content .important-news .page-image,
.front .tertiary-content .important-news .super-heading {
  display: none;
  padding: 0;
}
```

# 2.5.1

* Added update functions to remove old "mobil app" flags from the database.
* Updated openings hours panels plugins to only display "links" for opening hours that have content.


# Previous releases

This is changes in relation to DDB CMS (core) before this change log was started.

## Ding WAYF implementation
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/alma-wayf.diff
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/ddbasic-wayf.diff
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/ding_frontend-wayf.diff
* http://github.com/aakbcms/ding_wayf_dk.git

__Note__: AAKB uses "WAYF" directly and not DBC's gate-wayf.

## Opening hours
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/ddbasic-opening-hours.diff'
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/ding_library-opening-hours.diff
* https://www.drupal.org/files/issues/opening_hours-view_modes-2607314-6.patch


## Different permission changes:
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/ding_perm-override-node.diff
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/ding_perm-adv-user.diff
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/ding_perm-aakb-survey.diff

## Aakb survery
* https://github.com/ding2/ding2/compare/7.x-2.5.1...aakbcms:feature/ding_user_frontend-aakb_survey.diff
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
