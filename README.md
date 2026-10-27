from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.label import Label
from kivy.uix.button import Button

class BloxFriendsApp(App):
 def build(self):
  lay=BoxLayout(orientation='vertical',padding=20,spacing=15)
  lay.add_widget(Label(text="BLOX FRIENDS\n100% Compatibles",font_size=28,bold=True))
  b=Button(text="TROUVER MON AMI",background_color=(0,0.7,1,1),size_hint_y=0.3)
  b.bind(on_press=lambda x: setattr(self.res,'text',"Zoro_Daoukro 85%\nLuffy_Abidjan 90%"))
  lay.add_widget(b)
  self.res=Label(text="Clique pour trouver")
  lay.add_widget(self.res)
  return lay
BloxFriendsApp().run()
