Release Management
==================

The **Release Manager** is responsible for shepherding the release process to
successful completion. This document describes their responsibilities. Some items
must be done by people that have special privileges to do specific tasks
(e.g. privileges to access the production apt server),
but even if the **Release Manager** does not have those privileges, they should
coordinate with the person that does to make sure the task is completed.

Pre-Release
-----------

1. Open a **Release SecureDrop 0.x.y** issue to track release-related activity.
   Keep this issue updated as you proceed through the release process for
   transparency.
2. Check if there is a new stable release of Tor that can be QAed and released
   as part of the SecureDrop release. If so, file an issue.
3. Check if a release candidate for the Tails release is prepared. If so, request
   people participating in QA to use the latest release candidate.
4. Prepare a changelog describing the changes in the release.
5. Ensure that a pre-release announcement is prepared and shared with the community
   for feedback. Once the announcement is ready, coordinate with other team members to
   send them to current administrators, post on the SecureDrop blog, and tweet
   out a link.
6. For a regular release for version 0.x.0, branch off ``develop``:

  ::

     git checkout develop
     git checkout -b release/0.x

.. warning:: For new branches, please ask a ``freedomofpress`` organization
  administrator to enable branch protection on the release branch. We want to
  require CI to be passing as well as at least one approving review prior to
  merging into the release branch.

7. Prepare each release candidate where ``rcN`` is the Nth release candidate
   using this script:

  ::

     securedrop/bin/dev-shell ../update_version.sh 0.x.y~rcN

8. If you would like to sign the release commit, you will need to do so manually:

    a. Create a new signed commit and verify the signature:

      ::

         git reset HEAD~1
         git commit -aS
         git log --show-signature

    b. Ensure the new commit is signed, take note of the commit hash.

    c. Edit `0.x.y-rcN.tag` and replace the commit hash with the new (signed) commit
       hash.

    d. Delete the old tag and create a new one based on the tag file edited above:

      ::

         git tag -d 0.x.y-rcN
         git mktag < 0.x.y-rcN.tag > .git/refs/tags/0.x.y-rcN

9. Push the branch and tags.
10. Build Debian packages and place them on ``apt-test.freedom.press``.
11. Write a test plan that focuses on the new functionality introduced in the release.
    Post for feedback and make changes based on suggestions from the community.
12. Encourage QA participants to QA the release on production VMs and hardware. They
    should post their QA reports in the release issue such that it is clear what
    was and what was not tested. It is the responsibility of the release manager
    to ensure that sufficient QA is done on the release candidate prior to
    final release.
13. Triage bugs as they are reported, if a bug is important to fix and does not
    receive attention, you should fix the bug yourself or find someone who agrees
    to work on a fix.
14. Backport release QA fixes merged into ``develop`` into the
    release branch using ``git cherry-pick -x <commit>`` to clearly indicate
    where the commit originated from.
15. At your discretion - for example when a significant fix is merged - prepare
    additional release candidates and have fresh Debian packages prepared for
    testing.
16. For a regular release, the string freeze will be declared by the
    translation administrator one week prior to the release. After this is done, ensure
    that no changes involving string changes are backported into the release branch.
17. Ensure that a draft of the release notes are prepared and shared with the
    community for feedback.

Release Process
---------------

1. If this is a regular release, work with the translation administrator
   responsible for this release cycle to review and merge the final translations
   and screenshots (if necessary) they prepare. Refer to the 
   :ref:`i18n documentation <i18n_release>` for more information about the i18n 
   release process. Note that you *must* manually inspect each line in the diff 
   to ensure no malicious content is introduced.
2. Prepare the final release commit and tag. Do not push the tag file.
3. Step through the signing ceremony for the tag file. If you do not have
   permissions to do so, coordinate with someone that does.
4. Once the tag is signed, append the detached signature to the unsigned tag:

  ::

    cat 0.x.y.tag.sig >> 0.x.y.tag

5. Delete the original unsigned tag:

  ::

    git tag -d 0.x.y

6. Make the signed tag:

  ::

    git mktag < 0.x.y.tag > .git/refs/tags/0.x.y

7. Verify the signed tag:

  ::

    git tag -v 0.x.y

8. Push the signed tag:

  ::

    git push origin 0.x.y

9. Build Debian packages. People building Debian packages should verify and build
   off the signed tag.
10. Step through the signing ceremony for the ``Release``
    file(s) (there may be multiple if Tor is also updated along
    with the SecureDrop release).
11. Put signed Debian packages on ``apt-test.freedom.press``.
12. Coordinate with one or more team members to confirm a successful clean install
    in production VMs using the packages on ``apt-test.freedom.press``.
13. Put signed Debian packages on ``apt.freedom.press``. The release is now live.
14. Make sure that the default branch of documentation is being built off the tip
    of the release branch.
15. Make sure that release notes are written and posted on the SecureDrop blog.
16. Make sure that the release is announced from the SecureDrop Twitter account.

Post-Release
------------

After the release, carefully monitor the FPF support portal (or ask those that have access to
monitor) and SecureDrop community support forum for any issues that users are
having.
