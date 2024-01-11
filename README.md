# rhel_disable_KCM_cache
Disables the KCM credential cache by commenting out the libdefaults section. 

i.e.:
/etc/krb5.conf.d/kcm_default_ccache 

# This file should normally be installed by your distribution into a
# directory that is included from the Kerberos configuration file (/etc/krb5.conf)
# On Fedora/RHEL/CentOS, this is /etc/krb5.conf.d/
#
# To enable the KCM credential cache enable the KCM socket and the service:
#   systemctl enable sssd-kcm.socket
#   systemctl start sssd-kcm.socket
#
# To disable the KCM credential cache, comment out the following lines.

#[libdefaults]
#    default_ccache_name = KCM:
