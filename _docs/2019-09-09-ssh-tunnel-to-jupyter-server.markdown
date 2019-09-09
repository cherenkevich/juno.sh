---
layout: doc
title: "Connect to Jupyter server using SSH port forwarding"
description: "Follow these steps to connect to your own Jupyter server by establishing an SSH tunnel from Juno Connect on your iPhone or iPad"
image: ""
lang: "en_GB"
date: 2019-09-09 10:00:00
author: Alex Staravoitau
---

Juno Connect lets you use your Jupyter server remotely on your iPad or iPhone by either connecting directly (via HTTP/HTTPS), or by establishing a secure SSH tunnel and using SSH port forwarding. Follow these steps to connect to your server via SSH tunneling.  

<!--more-->

## Do I need this?

Juno Connect supports two types of connection: _Direct_ and _Port forwarding_. Which one to use depends on your particular circumstances, but generally speaking:

* It is easier and more secure to use **Port forwarding** connection. Especially so, if you plan to access your Jupyter server from _outside of your local network_ (i.e. over the internet).
* Alternatively, it should be reasonably safe to use **Direct connection** when you connect to a server _in your local network_ — say, your laptop or PC, which is connected to the same Wi-Fi. 

However, it should be possible to use either connection type for wherever you are connecting from, of course. This guide explains how to connect using SSH port forwarding, for direct connection see: [Connect to Jupyter server directly](/direct-connection-to-jupyter-server/){:target="_blank"}.

## Start your Jupyter server

Make sure your Jupyter instance is running on your server — you may need to start it on your desktop, or using one of iOS terminal apps with SSH support. 

Generally, you could simply SSH into your remote server, and run `jupyter notebook` in the terminal. However, typically you would like Jupyter to keep running even when you disconnect. To enable this, you may want to look into [screen](http://manpages.ubuntu.com/manpages/xenial/en/man1/screen.1.html){:target="_blank"}, or [Tmux (Terminal Multiplexer)](https://github.com/tmux/tmux/wiki){:target="_blank"}. For example, this is how you can start a Jupyter instance, and leave it running "in the background" using Tmux, no matter if you are still connected to the server or not.

```bash
# Connect to your server first
ssh user@your-server-address
# Start a new Tmux session
tmux new -s jupytersession
```

This will open a new session in terminal, where you can now start Jupyter. Use `--no-browser` option to ask Jupyter not to launch browser _on the server_.

```bash
# Start Jupyter in this new session
jupyter notebook --no-browser
```

Now detach from this session by pressing **Ctrl** + **D**, and then pressing **B**. This will send your Jupyter notebook instance to the background, and it will keep running even if you disconnect from your remote machine. 

If you want to stop this Jupyter instance, you can re-attach to the Tmux's `jupytersession` by connecting via SSH again, and running:

```bash
tmux a -t jupytersession
```

Now that Jupyter is running on your server, you can connect to it via SSH port forwarding from Juno Connect.

## Add server configuration in Juno Connect

Add a new server configuration, and make sure to select **Local port forwarding** as connection type.

<div style="text-align: center;">
    <img src="{{ "/images/docs/port_forwarding_connection.png" | prepend: site.baseurl }}" alt="Juno Connect direct connection settings">
</div>

### Connection settings

For **Host**, use your server's IP address or domain name. **Port** defaults to 22, which is the standard port for SSH — most likely, you won't need to change this setting.

### Authentication settings

**Username** should be the name of your server's user account that you connect as. Juno Connect supports authentication with password or private key — for the latter, you can either import your key from file or from clipboard. 

### Port forwarding settings

Most likely you won't need to change the **Host** setting, as it is set to `localhost`, and this is where your Jupyter instance is running — from your server's point of view. **Port** is set to Jupyter's default `8888`, but if it is running on some other port on your server, you should provide it here.

{:refdef: .notice}
<i class="fa fa-info-circle fa-2x" aria-hidden="true" style="color: #CCCCCC; vertical-align: middle;"></i><span style="display:inline-block; width: 8px;"></span> <span>Juno Connect will establish  SSH tunnel when you select your server in the list, and will try to load Jupyter's interface once connected. SSH connection should stay alive — it may even remain active for some time while Juno Connect is in the background, although iOS will eventually shut it down. To manually disconnect, go to server settings and select **Disconnect SSH Tunnel**.</span>
{: refdef}