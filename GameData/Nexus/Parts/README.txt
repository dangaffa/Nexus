Nexus, v1.1.0

INSTALLATION
Unpack to GameData folder of KSP.  Nexus" folder should be a sub-folder of GameData.  It then contains the parts within the Parts folder, and resources/flags etc in the other appropriate folders without interfering with regular KSP bits.

Reflection plugin is released as Public Domain as was the original plugin by Razchek and modified by Starwaster.
http://forum.kerbalspaceprogram.com/threads/70089-Reflection-Plugin-Continued-0-24-2

Assumes but does not require Community Tech Tree (Creative Commons Attribution-NonCommercial) by Nertea.
http://forum.kerbalspaceprogram.com/threads/100385-Community-Tech-Tree-2-0-last-updated-03-05-15?p=1546633#post1546633

Bundles Community Resource Pack by Rover Dude/USI.
http://forum.kerbalspaceprogram.com/threads/91998-1-0-4-Community-Resource-Pack-04-3-2015-07-06?highlight=community+resource

Remaining components are licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.  

Significant thanks need to go to Scott Lowther of up-ship.com/Aerospace Project Review and his work with the Nexus and related topics.  And to the mob of very useful people in the KSP G+ Community.  And to Winchell Chung in particular for providing the impetus to mod the hell out of Kerbal and his Orion mod, that this started as a lofting solution for.

The Nexus booster is a massive squat booster rocket designed by Convair (General Dynamics) to get very large payloads into orbit and beyond. This mod is a replica at half scale (Kerbals are small, and their planet is small) of the base Nexus design.

It was designed to get a million pounds (~450 tonnes) into orbit, and then return and be mostly re-usable. This version is designed for 1/8th of the weights/thrust of the original, to match the half scale.

Descent was controlled (but not really slowed) by big flaps. So side pieces are available as either flaps or static walls. You'll need 12 all up. Most representations have four flaps but versions with 12 were also investigated. Any mix of 12 pieces of either flap or static wall for KSP.  As yet, there's only the one style of flap, but I always intended to produce both types that are detailed in Convair documents, and have had Blender models for both since the start.  I just got these developed more as they look better than the whole panel and because I needed a test case to learn how to build aerobrakes in KSP.

At the last minute (I find just before the 1km altitude mark is best) forward facing solid rockets are fired that slow the descent and break the water surface tension and churn the water. This may have been optimistic, but probably would have worked as the forward shell/heat shield was sacrificial. A combination of this plus arrays of chutes was investigated but for some reason Convair decided to go with just the retro rockets. It apparently weighed less. Due to being lazy with determining re-entry points, I tend to add chutes. The retro rocket solution ain't so good landing on rock either.

Second stages so far are 35 foot and 60 foot hydrogen tanks with gas core rockets. So far there's 3 sizes, matching the 3 sizes used for the Convair 70 and 120 foot second stages. At 1/8th of 6 million pound thrust, and 4 and 3, it's easier to just refer to them by the original thrust grades. 
Gas Core Nuclear Thermal Rockets (GCRs) don't work well below a 1meter internal radius apparently (according to some studies around '98), so I'm being optimistic and saying Kerbals can make them a bit smaller. The 3MpT engine has an outside radius of 1m, so it's not too far off reality.  The GCRs, as represented in this mod, are moderately optimistic.  As yet, humanity hasn't managed to solve some fairly critical issues around instability of the containment vortex that stops the gaseous fission reaction from shifting and impacting things and then exploding.  

In KSP terms, be aware these rockets are both generators and alternators.  As the whole engine is mounted on a gimbal, they can gimbal a lot. Their atmospheric curve is highly punishing for using them in an atmosphere.  (Kerbals don't seem to care as much about the radioactive and toxic exhaust, but reduced Isp is bad).  They require a new resource, "BlutoniumTetraflouride", which is the reactor fuel.  Some is expended.  You'll get quite a bit of flight on the included fuel.  They also explode easily.  Not from their own operation, but just try not to bump them into things.

My original GCRs had a long slow build up and shut off time.  Much like the jet engines, throttle response was slow.  This is a result of my expectations of the engineering issues around building toroidal vortexes strong enough to hold a gaseous fission reaction.  But in testing attempts to land on the Mun, it became clear that I just couldn't work a successful landing with the exaggerated throttle response lag.  So this edition has that "feature" removed.  It's likely to be re-applied later.  But I'll be doing a bit of research into what that lag should be.  In the end case, either the rockets won't have lag, or they will and you'll be best off with some fine control secondary landing rockets.

RELEASE NOTES for 1.1.0
This is a structural alteration to folder structure to bring the Nexus into line with CKAN (hopefully).  This means, if you're updating manually, you should remove all sign of this mod first before updating.  The root folder has changed from Tiktaalik back to Nexus.
Other small changes: Fixed the floating attach nodes on top of the 70 foot fairing.  Changed the rescale for the Gas Core Rockets again so they actually rescale, and started working on heat/emissives for them (only functioning on the 6k GCR for now).

RELEASE NOTES for 1.0.5
I got around to doing the maths on the Isp adjustment due to the exhausting of the vaporized nozzle.  Turns out my guess was off by miles.  So I've adjusted that.  Also, in a youtube review I noticed the GCRs are all the same size.  They should all be rescaled, but there's always been an issue with the rescalefactor thingy.  They were all the same unity object, rescaled in config.  So I rescaled in Unity and now the configs are all x1.0, with resized mu files.

RELEASE NOTES for 1.0.4
This is an engine update release.  First up, the main plug engine had 60 nozzles that were released with a high res, small size edition that was basically a copy of the control rocket nozzle, with all that detail.  60 of them.  Where you can hardly see them.  They were always meant to get downgraded to a mesh with less polygons, but I plain forgot.  This is now done.  The texture is pretty simple, black nozzle, titanium pumps etc.  I'll tidy that up later, but keep it fairly low res.  
And a second engine type, the Rocketdyne L-30 AH Expansion Deflection rocket engine.  This replaces the plug and the control rockets.  I can't stop you adding control rockets of course, but the original design was just this one big puppy.  It "gimbals" like the plug engine, by differentially throttling the pumps feeding the combustion.  In this case there's five pumps feeding a toroidal combustion chamber.  Expansion deflection engines are basically a mix of traditional bell nozzles with a truncated aerospike inside.  Think of it as a shrouded aerospike.  The other piece of craziness with the L-30 was that instead of feeding fuel around and regeneratively cooling the nozzle, it uses what's called ablative cooling.  That is, the inside of the nozzle evapourates and erodes during flight.  This makes things simpler (esp when you have an inside and outside nozzle) but for something that's going to burn until orbit, it makes for a heavy nozzle.  I've modelled this using a multimode engine.  Primary mode burns through an ablator resource, and when it's used up, the secondary mode increases heat dramatically.  Also, as there's 40 tonnes of ablator, I've made it tweakable.  If you think you'll reach orbit early (less payload etc), then you can drop some ablator to drop some mass.  Use with caution.  :-)

RELEASE NOTES for 1.0.3
Some minor tweaks on exhaust effects for the LH2/LOX rockets.  If using stock, I've removed the smoke altogether, and if using RealPlume, the plume has been a bit tweaked for the Plug engine.
The real reason for this update is to get the updated fairings up there.  Old fairings had one single stack node of appropriate size on top.  New fairings have an array of size 2&3 nodes.  70 foot fairing has a central size 9 stack node and 8 size 2 nodes at 45degree spacing around it.  120 foot has a central size 15, then an inner circle of 6 size 3, then an outer circle of 6 each (alternating) size 3 and 2 stack nodes.

RELEASE NOTES for 1.0.2
Fixed community tech tree config, thanks Fizboy. MaverickSawyer spotted that there were no strength values on the retro decoupler. Spotted in the classic KSP sense of having things explode. This should be fixed. KeithS noticed the example craft files had disappeared. They've been added back in. Or two have been anyway. The 120 foot tank is slightly more developed.
I haven't looked at costs of parts at all. They're completely wrong, so they'll probably get fixed up shortly. Nexuses wouldn't have been cheap. And then it'll be on to the less optimistic second stages. Solid core and water moderated solid core NTRs. And some of the alternate engine arrangements for the base Nexus.

RELEASE NOTES for 1.0.1
All names of parts in feet changed to special Kerbal feet which are half human feet, or 0.1524m.  Which combined with the KSP Nexus being half scale for half sized Kerbals and to fit in the Hanger, means I can now refer to Nexus parts using their original sizes.  Similarly, pounds will refer to kerbal pounds, of which there's about 17.6kerbal pounds per kg.  This will break save games in as much as craft built using old parts will fail to load and create nasty pop ups you need to click on.
CTT config finished, but not working.  I'll look into that.
Re-applied plain black texture to the small adapters (120foot down to 3.75m).  They aren't textured yet, but you don't really need them.
Included more small tanks.  These will get textures and more fuel types (mono springs to mind).
Redid the 120foot segmented tank from scratch, plus the fairing for it.  Not properly textured just yet.

RELEASE NOTES for 1.0
60 foot (18.3m) fairing part is not yet done.  It will show as a stock Squad fairing that's been enlarged.  35f fairing is mostly done.
Misc/add-on tanks not yet complete.  No textures, etc and not the full set.  There will be radially mounted tanks as well for applying to the outside of things, as well as the short and extra short tanks currently included as LOX and LH variants (more variants likely to be created).
