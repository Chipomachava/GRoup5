<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Group Work Participation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #007BFF;
            color: #fff;
            padding: 1rem;
            text-align: center;
        }

        main {
            max-width: 800px;
            margin: 2rem auto;
            padding: 1rem;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        form {
            display: flex;
            flex-direction: column;
        }

        label {
            margin: 0.5rem 0;
        }

        input, select {
            padding: 0.5rem;
            margin-bottom: 1rem;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            padding: 0.75rem;
            border: none;
            background-color: #007BFF;
            color: #fff;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #0056b3;
        }

        #message {
            margin-top: 1rem;
            color: #28a745;
        }

        #feedback-list {
            margin-top: 1rem;
        }

        .feedback-item {
            padding: 0.5rem;
            border-bottom: 1px solid #ccc;
        }

        option[disabled] {
            background-color: #f0f0f0;
            color: #aaa;
        }
    </style>
</head>
<body>
    <header>
        <h1>Group Work Participation</h1>
    </header>
    <main>
        <h2>Select a Topic and Sign In</h2>
        <form id="participation-form">
            <label for="topic">Choose a topic:</label>
            <select id="topic" name="topic">
                <option value="Topic1">Topic 1</option>
                <option value="Topic2">Topic 2</option>
                <option value="Topic3">Topic 3</option>
                <option value="Topic3">Topic 3</option>
                <option value="Topic3">Topic 4</option>
                <option value="Topic3">Topic 5</option>
                <option value="Topic3">Topic 5</option>
                <option value="Topic3">Topic 6</option>
                <!-- Add more topics as needed -->
            </select>
            <label for="name">Your Name:</label>
            <input type="text" id="name" name="name" required>
            <button type="button" onclick="submitForm()">Submit</button>
        </form>
        <div id="message"></div>
        <div id="feedback-list">
            <h3>Feedback List:</h3>
            <div id="feedback-container"></div>
        </div>
    </main>
    <script>
        // Array to store feedback
        const feedbackList = [];

        function submitForm() {
            const topicSelect = document.getElementById('topic');
            const topic = topicSelect.value;
            const name = document.getElementById('name').value;
            const messageDiv = document.getElementById('message');
            const feedbackContainer = document.getElementById('feedback-container');

            if (name && topic) {
                // Add feedback to list
                feedbackList.push({ name, topic });

                // Disable the selected topic
                disableTopic(topic);

                // Display thank-you message
                messageDiv.textContent = `Thank you, ${name}. You have chosen ${topic}.`;

                // Update feedback list display
                displayFeedbackList();

                // Reset form
                document.getElementById('participation-form').reset();
            } else {
                messageDiv.textContent = 'Please enter your name and choose a topic.';
            }
        }

        function displayFeedbackList() {
            const feedbackContainer = document.getElementById('feedback-container');
            feedbackContainer.innerHTML = ''; // Clear previous content

            feedbackList.forEach(feedback => {
                const div = document.createElement('div');
                div.className = 'feedback-item';
                div.textContent = `${feedback.name} chose ${feedback.topic}`;
                feedbackContainer.appendChild(div);
            });
        }

        function disableTopic(selectedTopic) {
            const topicSelect = document.getElementById('topic');
            Array.from(topicSelect.options).forEach(option => {
                if (option.value === selectedTopic) {
                    option.disabled = true;
                }
            });
        }
    </script>
</body>
</html>
