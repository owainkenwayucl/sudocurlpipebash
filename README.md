# sudocurlpipebash://

## The URL handler we demand.

A significant number of extremnely high quality software ~~splats~~packages have an install process that requires users to curl a web URL, pipe it through bash and run it through `sudo`.  

```console
$ sudo "curl [url] | bash"
```

Sometimes, if the software is exceptionally high quality, the instructions will even [split this line into a multiple steps](https://clojure.org/guides/getting_started#_installation_on_linux).

This is very complicated and confusing for users and so in the same style as apt-url links, we demand (and plan to write) a URL handler which will allow developers of all types to create links users can click on to achieve this complete installation workflow with a click.

It's important to register a URL handler because it emables all sorts of useful workflows, such as allowing users to send each other `sudocurlpipebash://` links in chat apps to enable easier collaboration.

## Proposal

1. URLs will start `sudocurlpipebash://`
2. HTTPS will be default.  **Option:** `insecuresudocurlpipebash://` *for non-HTTPS?*
3. URL handler should use a graphical `sudo` agent where possible so that it makes use of previous authentications, preventing users from having to see a scary authentication box wherever possible.
4. There should be some whizzy animation that happens while the script is running.
5. Scripts must not ask the user any questions because that is scary and confusing.
6. There should be a command line interface so that it is possible to embed processing of `sudocurlpipebash://` URLs transparently within scripts.
7. Logging is forbidden. Logs contain confusing and upsetting information.
