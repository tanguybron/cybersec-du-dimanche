FROM ubuntu:20.04
RUN chmod 777 /etc/shadow

RUN useradd -ms /bin/bash martin

RUN sed -i -e 's,^root:[^:]\+:,root:$6$wrfEbymINR62oYga$wGAsQ5o7xTVNQednwovRIEtelhcaj/xXPv2vo5YhFODqjaGTCuNlhTvByM.EUuYVIIcEyxN5A/eLL6yHBxN9f/:,' /etc/shadow

USER martin
WORKDIR /home/martin
