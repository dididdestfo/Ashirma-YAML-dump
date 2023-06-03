#Backup copy of the snippet made for the goblin racefeat

!snippet fury <drac2>
args = argparse(&ARGS&)
cc = "Fury of the Small"
ch = character()
v=ch.cc_exists(cc) and ch.get_cc(cc)

if not ch.cc_exists(cc):
  return f""" -f "{cc}|You aren't a goblin!" """

elif not v:
  return f""" -f "{cc}|{ch.cc_str(cc)}
Small you are, furious you are not anymore!" """

else:
  die = min(ch.get_cc(cc), args.last('rr', default=1, type_=int))
  ch.mod_cc(cc, -die)
  return f""" -d{die} {proficiencyBonus} -f "{cc} -{die}|{ch.cc_str(cc)}
When you damage a creature with an attack or a spell and the creature's size is larger than yours, you can cause the attack or spell to deal extra damage to the creature. The extra damage equals your proficiency bonus.!" """
</drac2>
