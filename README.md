# creatingTgbot
Write this code after creating venv for Tgbot

    from aiogram import Bot, Dispatcher, executor, types
    
    bot = Bot(token='YOUR_BOT_TOKEN')
    
    dp = Dispatcher(bot=bot)
    
    
    @dp.message_handler(text='/start')
    async def cmd_start(msg: types.Message):
        print(msg.from_user.full_name, msg.text)
        await msg.answer(f"Hello {msg.from_user.full_name}!"
