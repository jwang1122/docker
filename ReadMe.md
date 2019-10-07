# Build simple docker container

[Docker tutorial](https://www.youtube.com/watch?v=Qw9zlE3t8Ko)

## First Pythong web application
1. install flask
```cmd
pip install flask
pip install flask_restful
```

2. create api.py
```python
from flask import Flask
from flask_restful import Resource, Api

app = Flask(__name__)
api = Api(app)

class Product(Resource):
    def get(self):
        return{
            'product': ['Ice cream',
                        'Chocolate',
                        'fruite']
        }

api.add_resource(Product, '/')

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=80, debug=True)
```

3. run the application
```cmd
sudo python api.py
password: qianjiang
```

4. stop the application: Ctrl+c