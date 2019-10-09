### Dockerfile - Exemplo

```yaml
FROM yannart/jboss-5.1.0.ga-jdk6

ENV AṔP_HOME=/opt/jboss/server/default/deploy

COPY *.ear ${APP_HOME}/agenda-packaging.ear

EXPOSE 8080 9990 8787
```