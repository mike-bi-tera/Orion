from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button

class MyAIApp(App):
    def build(self):
        self.layout = BoxLayout(orientation="vertical", padding=20, spacing=10)

        self.label = Label(text="Hello! I am your AI.", font_size=24)
        self.input = TextInput(hint_text="Type something...", multiline=False, size_hint_y=None, height=50)
        self.button = Button(text="Send", size_hint_y=None, height=50, on_press=self.respond)

        self.layout.add_widget(self.label)
        self.layout.add_widget(self.input)
        self.layout.add_widget(self.button)

        return self.layout

    def respond(self, instance):
        user_text = self.input.text.strip()
        if user_text == "":
            self.label.text = "Please type something!"
        elif user_text.lower() in ["hello", "hi"]:
            self.label.text = "Hi there! How are you?"
        elif user_text.lower() == "bye":
            self.label.text = "Goodbye 👋"
        else:
            self.label.text = f"You said: {user_text}"
        self.input.text = ""  # clear input

if __name__ == "__main__":
    MyAIApp().run()
