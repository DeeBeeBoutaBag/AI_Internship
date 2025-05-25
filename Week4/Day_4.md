## Day 4: Introduce Simple Flask Backend

- **Install Flask:**
    ```sh
    pip install flask
    ```

- **Build very basic API server:**
    ```python
    from flask import Flask, request, jsonify

    app = Flask(__name__)

    @app.route('/validate', methods=['POST'])
    def validate_json():
        data = request.get_json()
        # Use previous validation code here
        return jsonify({"status": "ok"})

    if __name__ == '__main__':
        app.run(debug=True)
    ```

- **Test in Postman or with curl.**

---
