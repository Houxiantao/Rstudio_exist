FROM rocker/binder:4.0.2
LABEL maintainer='your_name'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/Houxiantao/Rstudio_exist/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2020-11-05/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
