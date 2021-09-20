release: python3 manage.py makemigrations && python3 manage.py migrate
web: daphne vacc.asgi:application --port $PORT --bind 0.0.0.0 -v2