# To Run

https://airflow.apache.org/docs/apache-airflow/stable/start.html

export AIRFLOW_HOME=~/airflow

AIRFLOW_VERSION=2.10.4

PYTHON_VERSION="$(python -c 'import sys; print(f"{sys.version_info.major}.{sys.version_info.minor}")')"

CONSTRAINT_URL="https://raw.githubusercontent.com/apache/airflow/constraints-${AIRFLOW_VERSION}/constraints-${PYTHON_VERSION}.txt"

pip install "apache-airflow==${AIRFLOW_VERSION}" --constraint "${CONSTRAINT_URL}"

In a separate terminal run: airflow scheduler

Then, run: airflow webserver -p 8080

Go to: ocalhost:8080
