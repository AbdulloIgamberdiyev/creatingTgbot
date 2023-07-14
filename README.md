# creatingTgbot
Write this code after creating venv for Tgbot


  from aiogram import Bot, Dispatcher, executor, types
  
  bot = Bot(token='6359023502:AAEzYzpjuIzvjvmHycEZZBUfCQSvAXpKhR0')
  
  dp = Dispatcher(bot=bot)
  
  
  @dp.message_handler(text='/start')
  async def cmd_start(msg: types.Message):
      print(msg.from_user.full_name, msg.text)
      await msg.answer(f"Hello {msg.from_user.full_name}!"
