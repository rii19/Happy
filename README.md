# Happy
import { Client, Message } from 'discord.js';

// partials で必要な権限を設定する必要あり
const client = new Client({ partials: ['MESSAGE', 'CHANNEL'] });

client.on('ready', () => {
    // ここに起動したときの処理
    console.log('準備完了');
});

client.on('message', async (msg: Message) => {
    if (msg.author.bot) {
        return;
    }
    // ここにメッセージを受信したときの処理
});

client.login(process.env.DISCORD_TOKEN || 'no_token_found');

