# rpmport
The RPM Package Manager (RPM) is a powerful package management system capable of building computer software from source into easily distributable packages, installing, updating and uninstalling packaged software

The z/OS link/rename workaround uses the installed `libexec/rpm/rpm-fsm-helper`
executable to isolate cwd changes (addressing the review concern on PR #42).
`RPM_FSM_HELPER` selects its absolute path; the zopen environment sets this for
relocated installations. The helper is installed even with `INSTALL_RPMCONFIG=OFF`.
