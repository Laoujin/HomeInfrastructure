Home Infrastructure
===================

## Monitoring

- [Grafana](http://192.168.1.5:3000)
    - Login with: admin / ${GRAFANA_ADMIN_PASSWORD}

```sh
cd monitoring
cp .sample.env .env
docker-compose up -d
```

### Grafana Alert

- Alerting > Contact points > Create contact point > Slack
    - [Webhook Url](https://api.slack.com/apps) > Incoming Webhooks
- Alerting > Alert rules > New alert rule
    - `count_over_time({level="error"}[5m])`
