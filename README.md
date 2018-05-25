# Bot
  import asyncio
import discord
from discord.ext.commands import Bot

Boi = Bot(',')

@Boi.command(pass_context = True)
async def Msay(ctx, *args):
    mesg = 'Hello Boi'.join(args)
    await Boi.delete_message(ctx.message)
    return await Boi.say(mesg)
