m4_define([base_version], [6.0.100])
m4_define([git_revision],
          m4_esyscmd([git rev-parse HEAD | cut -c-7 | tr -d '\n']))
m4_define([git_commit_count],
          m4_esyscmd([git log --pretty=format: HEAD | wc -l | tr -d '\n']))
m4_define([date], m4_esyscmd([date +%Y%m%d | tr -d '\n']))
m4_define([fullversion], [base_version-git_commit_count-date[git]git_revision])

AC_INIT([eucalyptus-ansible], [fullversion])

PLAYBOOK_COMMIT=2d20cec168b0a18c762edc93af8247c1c2e49c8b
PLAYBOOK_ORG=appscale

AC_ARG_WITH(playbook-commit,
    [  --with-playbook-commit=<commit>       the ats-deploy commit],
    [PLAYBOOK_COMMIT="${withval}"])

AC_ARG_WITH(playbook-org,
    [  --with-playbook-org=<commit>       the ats-deploy organization],
    [PLAYBOOK_ORG="${withval}"])

AC_CONFIG_FILES([
    Makefile
])
AC_SUBST(PLAYBOOK_COMMIT)
AC_SUBST(PLAYBOOK_ORG)
AC_OUTPUT
