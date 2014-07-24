Fluid Content Elements for Twitter Bootstrap 4 (Elements)
============================================

What is it?
-----------

A collection of Twitter Bootstrap 4 Fluid Content Elements written for `EXT:fluidcontent`.

What does it do?
-----------

Provides the template files and TypoScript setup necessary to use the included elements.

How does it do it?
-----------

By leveraging the integration logic provided by `EXT:fluidcontent` - enabling use of specially constructed Fluid templates as
content elements, much like the Flexible Content Elements concept from TemplaVoila.

How is it installed?
-----------

Download, install the extension and include the static TypoScript configuration.

How is it used?
-----------

After installation and inclusion of the static TypoScript, the included content elements will be available as new content element
types when inserting new content.

When inserted, each content element contains a special panel with configuration specifying how to render the content element.

References
-----------

* https://github.com/FluidTYPO3/fluidcontent is a dependency - it is the integration necessary to render Fluid Content Elements


Migrating from 'EXT:fluidcontent_zf4'
----------

Aplly the following SQL::

    UPDATE tt_content
    SET tx_fed_fcefile = REPLACE(tx_fed_fcefile, 'fluidcontent_zf4', 'fluidcontent_twbs')
    WHERE tx_fed_fcefile REGEXP '^fluidcontent_zf4:.*'
