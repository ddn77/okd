Need to modify restricted scc before deployment:
$ oc edit scc restricted
Change runAsUser.Type to RunAsAny
