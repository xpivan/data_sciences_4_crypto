First you need to fetch the docker-compose.yaml with command:

curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.6.0/docker-compose.yaml'

See https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html

Setting the right airflow user:

mkdir -p ./dags ./logs ./plugins
echo -e "AIRFLOW_UID=$(id -u)" > .env

Initialize the database:

docker-compose up airflow-init

