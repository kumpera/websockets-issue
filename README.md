# Repro instructions

1) Provision a Mac with High Sierra and dotnetcore 2.1.4
2) Start chrome in remote debugging mode:

```
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --remote-debugging-port=9222

````

3) dotnet run this puppy.

4) Got to localhost:9222 in Chrome and pick any tab for debugging.
You must end up inside the debugger and it must be working.


5) Replace the port in the URL with 9300 and reconnect. IE:

```
http://localhost:9222/devtools/inspector.html?ws=localhost:9222/devtools/page/(140424F648EDA868E601B824F39AE2F5)

->

http://localhost:9222/devtools/inspector.html?ws=localhost:9300/devtools/page/(140424F648EDA868E601B824F39AE2F5)

```

6) It will disconnect after a few seconds.