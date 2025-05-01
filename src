
# using src code is not needed, it has tons of watermarks and credits and is partialy obfuscated but u can easily on obfuscate or just look for viruses

# its safe dumbasses

import tkinter as tk #line:1
from tkinter import ttk ,messagebox #line:2
from pynput import mouse ,keyboard #line:3
from pynput .mouse import Controller as MouseController ,Listener as MouseListener ,Button #line:4
from pynput .keyboard import Listener as KeyboardListener ,Key #line:5
import threading #line:6
import time #line:7
import os #line:8
import sys #line:9
import ctypes #line:10
EnableRCS =True #line:13
RecoilControlMode ="Low"#line:14
RcCustomStrength =6 #line:15
RequireToggle =True #line:16
ToggleKey ="caps_lock"#line:17
DelayRate =7 #line:18
toggle_state =False #line:20
pressed_buttons =set ()#line:21
mouse_controller =MouseController ()#line:23
presets ={"Low":3 ,"Medium":10 ,"High":14 ,"Ultra":18 ,"Insanity":22 ,"Custom":RcCustomStrength }#line:32
def update_strength ():#line:34
    global RecoilControlStrength #line:35
    if RecoilControlMode =="Custom":#line:36
        RecoilControlStrength =RcCustomStrength #line:37
    else :#line:38
        RecoilControlStrength =presets [RecoilControlMode ]#line:39
update_strength ()#line:41
def recoil_control ():#line:43
    while True :#line:44
        if EnableRCS and (not RequireToggle or toggle_state ):#line:45
            if Button .left in pressed_buttons and Button .right in pressed_buttons :#line:46
                mouse_controller .move (0 ,RecoilControlStrength )#line:47
                time .sleep (DelayRate /1000 )#line:48
        time .sleep (0.001 )#line:49
def on_press (O000OO00O00O00O0O ):#line:51
    global toggle_state #line:52
    if RequireToggle :#line:53
        try :#line:54
            if O000OO00O00O00O0O ==getattr (Key ,ToggleKey ):#line:55
                toggle_state =not toggle_state #line:56
        except AttributeError :#line:57
            pass #line:58
def on_click (O00OO0O0OO000OO00 ,OOOOO00O000O0OOOO ,O0O0O00OO00000O0O ,O00O00OOOOOOO000O ):#line:60
    if O00O00OOOOOOO000O :#line:61
        pressed_buttons .add (O0O0O00OO00000O0O )#line:62
    else :#line:63
        pressed_buttons .discard (O0O0O00OO00000O0O )#line:64
KeyboardListener (on_press =on_press ,daemon =True ).start ()#line:67
MouseListener (on_click =on_click ,daemon =True ).start ()#line:68
threading .Thread (target =recoil_control ,daemon =True ).start ()#line:69
def is_admin ():#line:72
    try :#line:73
        return ctypes .windll .shell32 .IsUserAnAdmin ()#line:74
    except :#line:75
        return False #line:76
def run_as_admin ():#line:78
    if not is_admin ():#line:79
        O000000O0OO00O000 =messagebox .askyesno ("Made by Bogi - Admin Permission","This app made by Bogi needs to run as administrator for full functionality.\n\nDo you want to restart it as admin?")#line:80
        if O000000O0OO00O000 :#line:81
            O000OOO00OO00OOOO =sys .argv [0 ]#line:82
            O0OOOO0OOO0000OOO =" ".join ([f'"{O00OO0OOOOO000OOO}"'for O00OO0OOOOO000OOO in sys .argv [1 :]])#line:83
            ctypes .windll .shell32 .ShellExecuteW (None ,"runas",sys .executable ,f'"{O000OOO00OO00OOOO}" {O0OOOO0OOO0000OOO}',None ,1 )#line:84
            sys .exit ()#line:85
def apply_settings ():#line:88
    global EnableRCS ,RecoilControlMode ,RcCustomStrength ,RequireToggle ,ToggleKey ,DelayRate #line:89
    EnableRCS =enable_var .get ()#line:90
    RecoilControlMode =mode_var .get ()#line:91
    RcCustomStrength =int (custom_strength_var .get ())#line:92
    RequireToggle =toggle_var .get ()#line:93
    ToggleKey =toggle_key_var .get ()#line:94
    DelayRate =int (delay_var .get ())#line:95
    presets ["Custom"]=RcCustomStrength #line:96
    update_strength ()#line:97
root =tk .Tk ()#line:100
root .title ("🎯 Made by Bogi | Recoil Control GUI")#line:101
root .geometry ("420x450")#line:102
root .configure (bg ="#1e1e1e")#line:103
style =ttk .Style ()#line:105
style .theme_use ("clam")#line:106
style .configure ("TLabel",background ="#1e1e1e",foreground ="#ffffff",font =("Segoe UI",10 ))#line:107
style .configure ("TButton",font =("Segoe UI",10 ),padding =6 )#line:108
style .configure ("TCheckbutton",background ="#1e1e1e",foreground ="#ffffff",font =("Segoe UI",10 ))#line:109
style .configure ("TCombobox",fieldbackground ="#2e2e2e",background ="#2e2e2e",foreground ="#ffffff")#line:110
def create_spacer (O0OO000O0OOO0OOOO ):#line:112
    O00O0O0OO0OO0OO0O =tk .Label (root ,text ="",bg ="#1e1e1e")#line:113
    O00O0O0OO0OO0OO0O .pack (pady =O0OO000O0OOO0OOOO )#line:114
run_as_admin ()#line:116
tk .Label (root ,text ="🔥 Made by Bogi RCControl 🔥",font =("Segoe UI",16 ,"bold"),bg ="#1e1e1e",fg ="#00ffae").pack (pady =10 )#line:118
enable_var =tk .BooleanVar (value =True )#line:120
ttk .Checkbutton (root ,text ="Enable Recoil Control (Made by Bogi)",variable =enable_var ).pack (pady =5 )#line:121
tk .Label (root ,text ="Made by Bogi - Recoil Control Mode:").pack (pady =3 )#line:123
mode_var =tk .StringVar (value ="Low")#line:124
ttk .Combobox (root ,textvariable =mode_var ,values =list (presets .keys ())).pack (pady =5 )#line:125
tk .Label (root ,text ="Made by Bogi - Custom Strength:").pack (pady =3 )#line:127
custom_strength_var =tk .StringVar (value ="6")#line:128
tk .Entry (root ,textvariable =custom_strength_var ,bg ="#2e2e2e",fg ="#ffffff").pack (pady =5 )#line:129
toggle_var =tk .BooleanVar (value =True )#line:131
ttk .Checkbutton (root ,text ="Require Toggle Key (Made by Bogi)",variable =toggle_var ).pack (pady =5 )#line:132
tk .Label (root ,text ="Made by Bogi - Toggle Key (caps_lock, num_lock, scroll_lock):").pack (pady =3 )#line:134
toggle_key_var =tk .StringVar (value ="caps_lock")#line:135
tk .Entry (root ,textvariable =toggle_key_var ,bg ="#2e2e2e",fg ="#ffffff").pack (pady =5 )#line:136
tk .Label (root ,text ="Made by Bogi - Delay Rate (ms):").pack (pady =3 )#line:138
delay_var =tk .StringVar (value ="7")#line:139
tk .Entry (root ,textvariable =delay_var ,bg ="#2e2e2e",fg ="#ffffff").pack (pady =5 )#line:140
create_spacer (10 )#line:142
ttk .Button (root ,text ="Apply Settings (Made by Bogi)",command =apply_settings ).pack (pady =10 )#line:143
create_spacer (5 )#line:145
tk .Label (root ,text ="Hold Left + Right Click to activate.\nPress your toggle key to turn on/off (if required).\n(Made by Bogi)",font =("Segoe UI",9 ),bg ="#1e1e1e",fg ="#888888").pack (pady =15 )#line:146
root .mainloop ()#line:148
