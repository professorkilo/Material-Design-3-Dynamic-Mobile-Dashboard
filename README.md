A modern Home Assistant dashboard built on Material Design 3 (MD3) principles, featuring dynamic colors, transparent card layouts, and a sleek, clean UI for an elegant smart home experience. 

This comprehensive dashboard unifies control and monitoring for **lights, switches, temperature and humidity sensors, rainfall, wind, UV index, radar, weather forecasts, alarms, Hue scenes, cameras, heat pumps, door and window sensors, and irrigation control** - all presented in one cohesive, visually refined interface designed for both functionality and aesthetic harmony.

[_v.6.0.0_](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/releases/tag/v6.0.0) brings several new cards and usability improvements. A new Person Card shows who is home or away, while the current weather card has been streamlined into a single-line layout that still preserves most key information. This release also adds a Location Tracker, Battery Monitoring card for real-time sensor battery status, and a WiFi QR scanner for easy guest network access. Lighting controls have been upgraded with custom button cards to apply transparancy, the Curtain card now uses a custom implementation for better performance, and the Hue scene room selector has been expanded to support more rooms. Additionally, Expander cards help keep rooms organized by allowing sections to be collapsed, and new UI animations enhance visual feedback across the dashboard. This update also fixes animation artifacts and improves responsiveness when changing Hue scenes.

# ✨ Features

**🎨 MD3 Theme Engine**

Unlock unlimited color combinations with a simple color picker - thanks to the amazing work of Material You Theme repository.

**👥 Per-User Styling**

Each family member can have their own unique style and colors. Perfect for customizing your phone, tablets, and shared devices.

**💡Community Inspired**

Several cards are inspired by the incredible work of others in the Home Assistant community. Credit will be detailed below.

# 🖼️ Dashboard Walkthrough

<img width="1920" height="1080" alt="1" src="https://github.com/user-attachments/assets/da37fa88-20ae-4c6a-b14e-a312d9bdd243" />


**Overview Page**


The Overview page gives you a quick view and control of what matters most. At the top, it displays the current date, time, and a notification bell to running task such as sprinkler, or camera feed when the door is open, etc

The [_weather summary_](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/greeting%2C%20alarmo%2C%20and%20notification%20bell) has been streamlined to fit one single line 

There is a new [_person card_](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/Person%20card)

**_Home Tab_**

The Home tab features cards designed for quick interaction. The first card shows indoor and outdoor temperatures with built-in climate controls in a clean, unified layout. Below this is a swipeable section where you can toggle room occupancy for climate control, room presence for lighting, and security cameras for quick on/off. These controls are used daily to interact with the backend automations. 

Underneath, there’s a “Now Playing” music card and a _[floating navigation bar](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/assets)_. The calendar is hidden behind this bar and can be accessed by swiping on the screen.

**_Events Tab_**

The Environment tab provides Google Calendar events from multiple calendar sources.

**_Active Tab_**

The Active tab filters and displays entities that are currently on or active. For example, it can show lights left on, open doors, and other active devices such lights, doors, windows, fans, light swiches, and curtains.

<img width="1920" height="1080" alt="2" src="https://github.com/user-attachments/assets/26a124e2-b8c5-4ff0-be47-e4d3c73a58b2" />

**_Components Used:_**
- [Auto-Entities](https://github.com/thomasloven/lovelace-auto-entities)
- [Button-Card](https://github.com/custom-cards/button-card)
- [Calendar Card Pro](https://github.com/alexpfau/calendar-card-pro)
- [Config Template Card](https://github.com/iantrich/config-template-card)
- [Custom Card Features](https://github.com/Nerwyn/custom-card-features)
- [Mini-Graph-Card](https://github.com/kalkih/mini-graph-card)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Navbar Card](https://github.com/joseluis9595/lovelace-navbar-card)
- [Paper Buttons Row](https://github.com/jcwillox/lovelace-paper-buttons-row)
- [Simple Swipe Card](https://github.com/nutteloost/simple-swipe-card)

**Pop Up Cards**

Pop-up cards are hidden within the Overview page and appear when you tap specific buttons or cards.

The _[Now Playing music card](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/now%20playing%20pop%20up%20card)_ can be accessed by tapping the floating music control mentioned earlier.

The [_Location Person_](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/Location%20Card%20Example) card displays the timeline of the person entities.

The _[Notifications card](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/notification%20center%20example)_ displays important items defined in your templates.yaml, such as chore management, active timers, live camera feeds when a door is opened, and sprinkler status.

The _[Alarmo card](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/alarmo%20card%20example)_ is opened by tapping the alarm icon in the top-right corner, allowing you to quickly arm or disarm the alarm system.


_**Components Used:**_
- [Alarmo Card](https://github.com/nielsfaber/alarmo-card)
- [Bubble Card](https://github.com/Clooos/Bubble-Card)
- [Location Timeline Card](https://github.com/konewka17/timeline_card)
- [Mediocre Hass Media Player Cards](https://github.com/antontanderup/mediocre-hass-media-player-cards)
- [Places](https://github.com/custom-components/places)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Timer Bar Card](https://github.com/rianadon/timer-bar-card)


<img width="1920" height="1080" alt="5" src="https://github.com/user-attachments/assets/bab83691-91f3-4d94-949b-6a1a1381a789" />


**Room Card Overview**

_[The Room Card Overview](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/Room%20Card%20example)_ gives you a quick snapshot of each room’s temperature and humidity, with the card color dynamically reflecting the current room status. Each card includes up to four customizable quick-action buttons for controls such as climate, lights, windows, doors, curtains, and fans. Tapping the room name takes you directly to that room’s dedicated page.


**_Components Used:_**
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Navbar Card](https://github.com/joseluis9595/lovelace-navbar-card)

<img width="1920" height="1080" alt="8" src="https://github.com/user-attachments/assets/dc3d140f-386e-487c-901e-2b42d07f91ee" />


**Scenes**

I love Philips Hue, but I decided not to use the bridge. Instead, I connected the lights directly to Zigbee2MQTT (Z2M) and rely on _[Hass Scene Preset](https://github.com/Hypfer/hass-scene_presets)_ to make the effects work without the bridge.
To activate a scene, I simply click the _[image representing the effect](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/hue%20scene%20image%20example)_ and select a room. This setup is made possible using a combination of powerful HACS components, automations, scripts, input booleans, input_number, and input texts. Check this _[folder]_(https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/hue%20asset) to set it up.

<img width="1920" height="1080" alt="6" src="https://github.com/user-attachments/assets/e7a9b727-d0b1-4767-80cd-70541964dfba" />
<img width="1920" height="1080" alt="7" src="https://github.com/user-attachments/assets/36cca1e0-748c-4fd5-834d-5db14f5e1862" />

**_Components Used:_**
- [Bubble Card](https://github.com/Clooos/Bubble-Card)
- [Button-Card](https://github.com/custom-cards/button-card)
- [Scene Presets](https://github.com/Hypfer/hass-scene_presets)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Navbar Card](https://github.com/joseluis9595/lovelace-navbar-card)


**Individual Room Page**

I have transitioned away from dedicated room sections in favor of a Boolean-triggered Popup system. Now, for the above example, I have three buttons to show / hide more contents (Other Lights, Bathroom) that stay hidden until called upon, keeping the main view focused.
Further down, there are _[three tabs](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/individual%20room%20page%20tabs)_:

- Room Tab: Contains light entities and a popup card for additional lights, as well as other elements like covers, media, switch, or anything else relevant to the room.

- Climate Tab: Displays climate controls for the room and shows humidity levels. In this example, the humidity is too high, so the indicator color appears red.

- Active Tab: This tab only appears when something in the room is active - such as an open door or window.

<img width="1920" height="1080" alt="3" src="https://github.com/user-attachments/assets/8c7b047d-8095-4899-a440-f4b3a9dbec3c" />
<img width="1920" height="1080" alt="4" src="https://github.com/user-attachments/assets/76d19881-16c6-49af-8d67-3794bbc0c5ba" />

**_Components Used:_**
- [Auto-Entities](https://github.com/thomasloven/lovelace-auto-entities)
- [Big Slider Card](https://github.com/nicufarmache/lovelace-big-slider-card)
- [Button-Card](https://github.com/custom-cards/button-card)
- [Custom Card Features](https://github.com/Nerwyn/custom-card-features)
- [Material Home Component](https://github.com/giovannilamarmora/lovelace-material-components)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Paper Buttons Row](https://github.com/jcwillox/lovelace-paper-buttons-row)
- [Simple Tabs Card](https://github.com/agoberg85/home-assistant-simple-tabs)


**Weather Panel**

The _[comprehensive weather panel](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/weather%20panel_)_ is a popup card accessible by clicking any of the weather forecast buttons at the top of the Overview page (as mentioned earlier).
Some tabs may be hidden when there are no active events - for example, if there are no earthquakes or volcanic activities at the moment.

This panel includes the following components:

- Earthquake
- Volcano
- Warning
- Weather Forecast
- Rainfall
- UV
- Wind
- Radar
 -Lunar

Each section highlights the next significant forecasted event.
For example, the Wind section displays when the strongest forecasted wind is expected and its intensity, while the chart below shows the current wind speed in real time.

**_Components Used:_**
- [Apex Charts Card](https://github.com/RomRider/apexcharts-card?tab=readme-ov-file#series-options)
- [Bubble Card](https://github.com/Clooos/Bubble-Card)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Lunar Phase Card](https://github.com/ngocjohn/lunar-phase-card)
- [Lunar Phase Integration](https://github.com/ngocjohn/lunar-phase)
- [Simple Tabs Card](https://github.com/agoberg85/home-assistant-simple-tabs)
- [World's Air Quality Index](https://www.home-assistant.io/integrations/waqi/)
- [Weather Card Extended](https://github.com/Thyraz/weather-forecast-extended)

<img width="1920" height="1080" alt="9" src="https://github.com/user-attachments/assets/d15e7d8e-517f-4578-aa98-871f9890d106" />


**Camera**

The _[_Cameras](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/camera%20tabs%20example)_ displays live camera feeds from each area, showing the last detected activity along with controls for nearby lights for quick actions.

<img width="1920" height="1080" alt="10" src="https://github.com/user-attachments/assets/2395d0d3-5e98-4f0a-82be-5066f307584a" />

**_Components Used:_**
- [Alarmo Card](https://github.com/nielsfaber/alarmo-card)
- [Bubble Card](https://github.com/Clooos/Bubble-Card)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Navbar Card](https://github.com/joseluis9595/lovelace-navbar-card)
- [Simple Tabs Card](https://github.com/agoberg85/home-assistant-simple-tabs)
- [Web RTC Camera](https://github.com/AlexxIT/WebRTC)

  
**Irrigation**

The irrigation page shows the current weather restriction level, along with _[tabs for different irrigation zones](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/irrigation%20page)_. It includes details such as each zone’s water valve status, the last run time, and direct controls for each valve - all presented with a clear, visually rich graph.

Below that, the system displays soil moisture levels, color-coded according to dryness, as well as the soil temperature for each zone.

Additionally, automations and scripts are used to control the valves, including phone notifications when the sprinklers turn on or off.

**_Components Used:_**
- [Config Template Card](https://github.com/iantrich/config-template-card)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Paper Buttons Row](https://github.com/jcwillox/lovelace-paper-buttons-row)
- [Simple Tabs Card](https://github.com/agoberg85/home-assistant-simple-tabs)


# Other Components:

Theme / Layout:

- [Material Symbols](https://github.com/beecho01/material-symbols)
- [Material You Theme](https://github.com/Nerwyn/material-you-theme)
- [Material You Utilities](https://github.com/Nerwyn/material-you-utilities)
- [Kiosk Mode](https://github.com/maykar/kiosk-mode)
- [Stack In Card](https://github.com/custom-cards/stack-in-card)
- [Streamline Card](https://github.com/brunosabot/streamline-card)
- [Vertical Stack In Card](https://github.com/ofekashery/vertical-stack-in-card)


# Installation

**For new user:**
- Copy all the code from _[full dashboard yaml](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/dashboard.yaml)_ to a new dashboard raw configuration editor to jumpstart your experience.
- Install the required HACS components (such as simple swipe card, stack-in-card, popup-card, etc. - see your setup for what’s needed).
- To unlock the full functionality (like weather icons, notification counts, and more), you’ll need to add the corresponding [sensors](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/template%20sensor) to your config.
- For the Hue scene, you'll need to have the automation, scripts, input boolean, input text, and input number in your system that you can find in [hue asset folder](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/hue%20asset). For the images, you can get them from [here](https://github.com/Hypfer/hass-scene_presets/blob/master/custom_components/scene_presets/assets/Readme.md).
- Apply the MD3 theme and select your preferred colors. It is accessible from Overview page > More > Bucket Fill Icon
- Apply [wallpaper](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/wallpaper/) (optional)
- Set the companion app to full screen (optional)

**For existing user:**
- Review the [streamline_template](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/blob/main/assets/streamline_templates) to see if you want to add / modify the previous version to the new version.
- Choose which card / visuals that you like to be added to your installation by clicking the hyperlink provided in the description above.
- Apply [wallpaper](https://github.com/ElementZoom/Material-Design-3-Dynamic-Mobile-Dashboard/tree/main/wallpaper/) (optional)
- Set the companion app to full screen (optional)

# 📚 Credits

This project builds upon the work of:
- Nerwyn – [Material You Theme](https://github.com/Nerwyn/material-you-theme) & [Material You Utilities](https://github.com/Nerwyn/material-you-utilities)
- [MySmartHome](https://www.youtube.com/@My_Smart_Home) - for the new simple tabs card, button cards styling, sliders, etc
- Other community members who kindly shared their cards

# 💖 Support My Work  

If you want to hire me to make your personal dashboard, you can hit me up on one of these social media platforms below:
- Email at  _reynaldi.sutrisno.rs16@gmail.com_
- [Reddit](https://www.reddit.com/u/ElementZoom/s/dr4NN0mTtj)
- [Facebook](https://www.facebook.com/profile.php?id=61578092475703)

Or you can support me on [Ko-fi](https://ko-fi.com/ElementZoom).
Your support helps me keep creating and sharing more awesome open-source tools! Thank you for being part of this journey 🚀
