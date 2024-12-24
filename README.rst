from telegram.ext import Updater, CommandHandler

#7833891933:AAFwarS7WLuj9GuTJ5a5vJ2WS4KAHjGhOqg
TOKEN = '7833891933:AAFwarS7WLuj9GuTJ5a5vJ2WS4KAHjGhOqg'
def start(update, context):
    update.message.reply_text('مرحبًا! أنا بوت تليجرام الخاص بك.')

def main():
    updater = Updater(TOKEN, use_context=True)
    dp = updater.dispatcher
    dp.add_handler(CommandHandler('start', start))
    updater.start_polling()
    updater.idle()

if __name__ == '__main__':
    main()
