DayZ New 1.30 Animaldogs Event Added To Livonia Map Mod Files For Console and PC Community Servers Instructions & Terms Of Use

When installed correctly these files will add the guard dogs to your Livonia Map. The dogs will mainly be in urban areas.

Limited Testing on PC Livonia Local PC Server, DAYZ Version 1.30 Nov 26.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files necessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recommend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Stop your server.

Upload the files livonia_dobermann_shepherd_territories.xml & animaldogs_livonia_event.xml from the extracted folder to inside the "custom" folder of the Livonia mission directory on your server.
(If you haven't got a "custom" folder, create one.)

Next open up your vanilla cfgenvironment.xml, and near the top,

below <file path="env/zombie_territories.xml" />

paste this: 

	<file path="custom/livonia_dobermann_shepherd_territories.xml" />

next, a little bit further down under

	<territory type="Herd" name="Bear" behavior="BlissBearGroupBeh">
			<file usable="bear_territories"/>
		</territory>
		
paste this:

<territory type="Herd" name="Dog" behavior="DZDogGroupBeh">
			<file usable="livonia_dobermann_shepherd_territories" />
		</territory>
		
		
save and upload the file where necessary.

Next open up your vanilla cfgeconomycore.xml, and near the bottom, above the closing

</economycore>

tag,

paste this:

	<ce folder="custom">
	<file name="animaldogs_livonia_event.xml" type="events" />
	</ce>

If you are already using files to append your vanilla mission files, it should look something like this:

<ce folder="custom">
	<file name="some-other-types-file.xml" type="types" />
	<file name="some-other-events.xml" type="events" />
	<file name="animaldogs_livonia_event.xml" type="events" />
	<file name="some-other-messages.xml" type="messages" />
	<file name="some-other-globals.xml" type="globals" />
	</ce>

Save the file.

Upload where necessary.

Validate your edited files to check you haven't made any mistakes with https://www.xmlvalidation.com/

Restart your server & changes should start to take effect.

----------

Dominus vobiscum! scalespeeder

GOOD LUCK!