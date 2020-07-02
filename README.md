# rhasspyexamples
This is a rhasspy example for Home Assistant and Node-Red

## IMPORTANT ##

- This is not a maintained GIT repository neither do I offer support for this. It is work in progress and should help others to take it as an example and make their own stuff from it.
- It is mostly german, if you prefer another language you have to translate slots and sentences.
- I removed most stuff from the slot files as I don't want to give detailed information about my home to everybody ;) However I left some examples in.
- Might contain a lot of bugs.
- This was built out of another example found in the Home Assistant community, which was built out of an rhasspy example flow.
- I might help with issues when I am available but it might also happen that you don't see me here for a while ;)

## Features: ##

- Controls light, covers, climate and hue scenes with rhasspy through Home Assistant and Node-Red using your HA entity names.
- If you don't specify a room / location it will use the siteId of the rhasspy or satellite you talk to.
- If you add "all" to the slot files, saying "all" instead of specifying an entity will switch ALL entitys of that domain.
- When you got it running, to use new entities from HA you only need to add how you wamnt to call them and their friendly name to the slot files. No need to alter the Node-Red flow or something else.

## WHAT YOU NEED TO DO TO USE IT RIGHT AWAY ##

- Import the Node-Red flow
- Import the ini files to rhasspy and fill them or create your own ones or just copy and paste and add your own stuff.
- In the Node-Red flow, replace the server names in the webhook node in the beginning and speech nodes at the end with you rhasspy / satellites.
- Select your Home Assistant Server in the svc nodes.
- Fill the slot files, I only left some examples in.
- Create groups in Home Assistant for your room (i.e. light.living_room, covers.kitchen) and fill them to the slots together with the other entities. You are free to create more groups as you like to and use them.
- To get the siteId feature working, name your rhasspy / satellite like the group for the room it sits in (i.e. kitchen).

## HINT ##

When you restart your rhasspy, i.e. because you changed the wakeword options or something, the webhook will loose the connection. If that happens you have to redeploy or restart your Node-Red flow to connect it again.
