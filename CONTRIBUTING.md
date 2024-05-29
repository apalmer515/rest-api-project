'''
FROM python:3.10
EXPOSE 5000
WORKDIR /app
COPY ./requirements.txt requirements.txt
RUN pip install --no-cache-dir --upgrade -r requirements.txt
COPY . .
CMD ["flask", "run", "--host", "0.0.0.0"]
'''

## HOW TO RUN DOCKERFILE LOCALLY


'''
docker run -dp 5005:5000 -w /app -v ${PWD}:/app IMAGE_NAME sh -c "flask run"
'''