jQuery Bracket library
======================

jQuery bracket is a jQuery plugin that lets users create and display single and
double elimination brackets for tournament play.

Feedback can be sent via mail to teijo(a)aropupu.fi or via IRC to Aroppuu @
IRC/Quakenet. If you've found use for this script, I'd be happy to hear about
it. Drop me a link and let me know if it can be shared on this project page.

Download
--------

Get latest pre-compiled version from `dist/`.

Building
--------
*   Install node
*   Run `npm install -g typescript` to install TypeScript globally
*   Run `npm install` to get dependencies
*   Install Ruby compass `gem install compass`
*   Run `grunt watch` to auto-compile changed files in src/
*   Run `grunt` to compile once

Minified files are compiled to `dist/` directory.

Examples
--------

Examples can be found from the project site at http://www.aropupu.fi/bracket/

Changes
-------

*   2013-10-29: Remove redundant styles. Make HTML more standards compliant.
    Streamline CSS and HTML to some extent with jQuery Group plugin. Markup
    and CSS in this release **are not backwards compatible!**
*   2013-10-07: `skipSecondaryFinal` boolean to finish double elimination
    tournament after first match. Skips the second match normally created if
    LB winner wins the first match. Display '--' score for non-played matches.
    Project ported to TypeScript with additional refactorings (not visible for
    library users).
*   2013-06-05: `onMatchHover` and `onMatchClick` callbacks created in order
    to allow more interaction with the bracket.
*   2013-04-03: "skipConsolationRound" option, minified distribution files
*   2013-03-14: Reversing the bracket flow with dir property
*   2012-07-10 (release 5): IE 8 support and remove "disabled" attributes as
    it messed IE8+ colors.
*   2012-07-09 (release 4): Included following fixes and added bubble for 4th
    place.
    *   There is no support for second final match. If LB winner wins the
        first round in finals, you must practically score the match according
        to rounds, e.g. 1-0, 0-1 or 0-2. In the fix if LB winner wins first
        final match, a new round will be created. Fix not perfectly backwards
        compatible. LB winning brackets with old results will be displayed
        unresolved as new final round is generated.
    *   Losers from WB will be assigned in same order to LB. This means that
        participants will have to play against previous opponents earlier than
        necessary. This fix is not backwards compatible! Every second round of
        WB losers will be assigned in reverse order to LB in order to maximize
        the time it takes for two teams to play against each other twice.
*   2012-04-09 (release 3): Fix bug preventing edit click of finalist in
    Firefox and Chrome.
*   2012-01-23: SASS conversion for styles. Fix bug with 2 teams.
*   2012-01-15 (release 2): Result labels and color adjustments.
*   2011-10-18 (release 1): Consolidation final support for single
    elimination.
*   2011-10-11: Bugfix: Zero not properly accepted as a result
