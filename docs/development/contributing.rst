Contributing to SecureDrop
==========================

Thank you for your interest in contributing to SecureDrop! We welcome both new
and experienced open-source contributors and are committed to making it as easy
as possible to contribute. Whether you have a few minutes or many hours, there
are a variety of ways to help. We are always looking for help from

* `programmers`_, to help us develop SecureDrop;
* `DevOps`_ people, to work on the community-maintained SecureDrop infrastructure;
* `release managers`_, to create and maintain Debian GNU/Linux packages and repositories;
* `writers`_, to help improve the documentation;
* `translators`_, to translate SecureDrop;
* `designers`_, to help improve the source and journalist web interfaces and Tails customization;
* `moderators and support`_ volunteers, to help with the support forums.

You can always find a developer to answer any questions you may have on the
`SecureDrop instant messaging channel
<https://gitter.im/freedomofpress/securedrop>`__. You can also register on `the
forum <https://forum.securedrop.club/>`__ for more information and to
participate in longer discussions.

.. note:: Not sure where to start? You can always ask for advice in the `chat
          room <https://gitter.im/freedomofpress/securedrop>`__.


Programmers
~~~~~~~~~~~

The SecureDrop system includes `Flask`_-based web applications for sources and
journalists. It is deployed across multiple machines with `Ansible`_. Most of
SecureDrop's code is written in `Python`_.

.. _`Flask`: http://flask.pocoo.org/
.. _`Ansible`: https://github.com/ansible/ansible
.. _`Python`: https://github.com/freedomofpress/securedrop/search?l=python

The following links should help you find something to work on:

Bugs
----

* `High-priority bugs <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3AP-high+label%3Abug>`__
* `Middle-priority bugs <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3Abug>`__
* `Low-priority bugs <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3AP-low+label%3Abug>`__

Issues Sorted by Topic
----------------------

* `User experience <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3AUX>`__
* `Internationalization (i18n) <https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3A%22goals%3A+i18n%22>`__
* `Source and journalist applications <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3Aapp>`__
* `Application code cleanup <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22goals%3A+app+code+cleanup%22>`__
* `SecureDrop Workstation <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22SecureDrop+Workstation%22>`__
* `Source experience <https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3A%22goals%3A+improve+source+experience%22>`__
* `Journalist experience <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22goals%3A+journalist+experience%22>`__
* `Ansible logic/installation <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22goals%3A+Improve+Ansible+logic+%2F+smoother+install%22>`__
* `Operations and deployment <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3Aops%2Fdeployment>`__
* `Threat model <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22goals%3A+improve+threat+modeling%22>`__
* `IDS noise <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22goals%3A+reduce+IDS+noise%22>`__
* `OSSEC <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3AOSSEC>`__
* `Security <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3Asecurity>`__
* `Research <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3Aresearch>`__

Development Environment
-----------------------

* `Developer workflow <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22goals%3A+improve+developer+workflow%22>`__
* `Tests <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22goals%3A+more+tests%22>`__
* `Continuous Integration <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-desc+label%3A%22goals%3A+sick+CI%22>`__

When you're ready to share your work with the SecureDrop team for review, submit
a `pull request
<https://help.github.com/categories/collaborating-with-issues-and-pull-requests/>`__
with the proposed changes. :doc:`Tests <testing_securedrop>` will run
automatically on GitHub.

If you would like to contribute on a regular basis, you'll want to read the
:doc:`developer documentation <setup_development>` and set up a local
development environment to preview changes, run tests locally, etc.


Writers
~~~~~~~

Technical writers and editors are invited to review the `documentation
<https://docs.securedrop.org/>`__ and fix any mistakes in accordance with the
:doc:`documentation guidelines <documentation_guidelines>`.

If this is your first time helping with SecureDrop documentation, consider
working on `low-hanging fruit`_ to become familiar with the process.

.. _`low-hanging fruit`: https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3Adocs+label%3AP-easy

Documentation Issues
--------------------

* `High-priority <https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3Adocs+label%3AP-high>`__
* `Middle-priority <https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3Adocs>`__
* `Low-priority <https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3Adocs+label%3AP-low>`__


DevOps
~~~~~~

The `SecureDrop web site <https://securedrop.org>`__ and the `GitHub repository
<https://github.com/freedomofpress>`__ are controlled and maintained by `Freedom
of the Press Foundation employees <https://freedom.press/about/staff>`__. The
resources under the ``securedrop.club`` domain name are financed, controlled,
and maintained by a horizontally organized `community of volunteers
<https://securedrop-club.readthedocs.io/en/latest/team.html>`__. You will find a
list of the pending tasks to improve the ``securedrop.club`` services in the
`contribution guide
<https://securedrop-club.readthedocs.io/en/latest/contribute.html>`__. If you're
in doubt, feel free to reach out to the `DevOps section of the forum
<https://forum.securedrop.club/c/devops>`__ or directly to `a team member
<https://securedrop-club.readthedocs.io/en/latest/team.html>`__.


Release Managers
~~~~~~~~~~~~~~~~

All software deployed with SecureDrop is installed via Debian GNU/Linux packages
via Ansible. The `primary repository <https://apt.freedom.press/>`__ is
controlled, maintained, and signed by `Freedom of the Press Foundation employees
<https://freedom.press/about/staff>`__. An `alternative repository
<https://packages.securedrop.club/>`__ signed by a `community of volunteers
<https://securedrop-club.readthedocs.io/en/latest/team.html>`__ is used only for
tests and demonstrations. The current responsibilities of the release manager
are covered in :doc:`detailed documentation <release_management>`.

If you are a `Debian developer <https://www.debian.org/devel/>`__ you can help
improve packaging and the release process:

* `Building SecureDrop application and OSSEC packages <https://github.com/freedomofpress/securedrop/blob/develop/install_files/ansible-base/build-deb-pkgs.yml>`__ and `pending bugs and tasks <https://github.com/freedomofpress/securedrop/issues?q=is%3Aissue+is%3Aopen+package+label%3A%22goals%3A+packaging%22>`__
* Building `grsecurity kernels <https://github.com/freedomofpress/ansible-role-grsecurity>`__ and `pending bugs and tasks <https://github.com/freedomofpress/ansible-role-grsecurity/issues>`__


Translators
~~~~~~~~~~~

All are kindly invited to help translate SecureDrop `using the Weblate interface
<https://weblate.securedrop.club/>`__. We provide a :doc:`detailed guide <l10n>`
to use as reference for details such as the meaning of placeholders, etc. Feel
free to reach out on the `translation section of the forum
<https://forum.securedrop.club/c/translations>`__ for help. Non-English forum
discussions are welcome to help facilitate translations.

As a developer or system administrator you can also help `maintain and improve
<http://securedrop-club.readthedocs.io/en/latest/weblate.html>`__ the
self-hosted `Weblate <https://weblate.org/>`__ infrastructure used by the
community of translators.


Designers
~~~~~~~~~

If you have web design or user experience design skills, take a look at these issues on GitHub:

* `User experience <https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3AUX>`__
* `CSS/SASS <https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3ACSS%2FSASS>`__ and `HTML <https://github.com/freedomofpress/securedrop/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3AHTML>`__
* `Journalist user experience <https://github.com/freedomofpress/securedrop/issues?q=is%3Aopen+is%3Aissue+label%3A%22goals%3A+journalist+experience%22>`__


Moderators and Support
~~~~~~~~~~~~~~~~~~~~~~

Those running a production instance of SecureDrop are encouraged to `read the
support documentation <https://securedrop-support.readthedocs.io/>`__ to get
help from the `Freedom of the Press Foundation <https://freedom.press>`__. For
less sensitive topics such as running a demo or getting help to understand a
concept, a `public forum section <https://forum.securedrop.club/c/support>`__ is
better suited. To assist on the forum:

* Look for `the latest unanswered questions in the
  <https://forum.securedrop.club/c/support>`__ forum and answer them.
* If you find questions `elsewhere in the forum
  <https://forum.securedrop.club>`__ that have a better chance at
  getting an answer in the `support section
  <https://forum.securedrop.club/c/support>`__, ask a `a team member
  <https://securedrop-club.readthedocs.io/en/latest/team.html>`__ for
  permissions to move topics from a category to another.
