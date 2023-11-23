Example:

<pre><code>
    case "main":
			try {
				var data = fs.readFileSync('command/menu.txt', 'utf8');
				m.reply(data.toString())
			}catch (error) {
				  if (error.response) {
					console.log(error.response.status);
					console.log(error.response.data);
					console.log(`${error.response.status}\n\n${error.response.data}`);
				  } else {
					console.log(error);
					m.reply("Maaf, sepertinya ada kesalahan :"+ error.message);
				  }
				}
        break;
</code></pre>
