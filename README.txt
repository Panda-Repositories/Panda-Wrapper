Hosted+

How to add Hosted+ to your project:

1. Include the files in your project directory, and inside the project.
2. Project Properties -> VC++ Directories -> Library Directories

$(MsBuildProjectDirectory)\Hosted+\cURL
$(MsBuildProjectDirectory)\Hosted+\JSON

3. Project Properties -> Linker -> Input

libcurl_a.lib
jsoncpp.lib
Ws2_32.lib
Wldap32.lib
crypt32.lib
Normaliz.lib

4. Project Properties -> Preprocessor ->

CURL_STATICLIB

5. Apply then your goot to go.

How to use Hosted+:

to get started u firts do:
HostedPlus::run();

To get the address you can do
HostedPlus::json["addresses"]["addr name"]["addr"]

To get the conv you can do
HostedPlus::json["addresses"]["addr name"]["cc"]

To add an function u can do:
auto function = HostedPlus::CreateDef<typedef,args...>("addr name");