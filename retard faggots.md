# Retard Pasting from [UnknownCheats](https://www.unknowncheats.me/forum/counter-strike-2-a/576077-counter-strike-2-reversal-structs-offsets.html)
    
### 8th February 2024 
```
C_PlantedC4 {
         m_bBombTicking = 0xED8;
         m_nBombSite = 0xEDC;
         m_nSourceSoundscapeHash = 0xEE0;
         m_entitySpottedState = 0xEE8;
         m_flNextGlow = 0xF00;
         m_flNextBeep = 0xF04;
         m_flC4Blow = 0xF08;
         m_bCannotBeDefused = 0xF0C;
         m_bHasExploded = 0xF0D;
         m_flTimerLength = 0xF10;
         m_bBeingDefused = 0xF14;
         m_bTriggerWarning = 0xF18;
         m_bExplodeWarning = 0xF1C;
         m_bC4Activated = 0xF20;
         m_bTenSecWarning = 0xF21;
         m_flDefuseLength = 0xF24;
         m_flDefuseCountDown = 0xF28;
         m_bBombDefused = 0xF2C;
         m_hBombDefuser = 0xF30;
         m_hControlPanel = 0xF34;
         m_hDefuserMultimeter = 0xF38;
         m_flNextRadarFlashTime = 0xF3C;
         m_bRadarFlash = 0xF40;
         m_pBombDefuser = 0xF44;
         m_fLastDefuseTime = 0xF48;
         m_pPredictionOwner = 0xF50;
         m_vecC4ExplodeSpectatePos = 0xF58;
         m_vecC4ExplodeSpectateAng = 0xF64;
         m_flC4ExplodeSpectateDuration = 0xF70;
    }
```
```
    for (int i = 1; i <= interfaces::g_game_resouce->entity_system->GetHighestEntityIndex(); i++)
    {
    	C_BaseEntity* entity = interfaces::g_game_resouce->entity_system->Get(i);
    	if (!entity || !entity->IsBasePlayerController() || entity->IsBasePlayerWeapon()) continue;
     
    	CCSPlayerController* controller = interfaces::g_game_resouce->entity_system->Get<CCSPlayerController>(entity->GetRefEHandle());
    	if (!controller) { continue; }
     
    	if (controller == sdk::local_controller || controller->m_iTeamNum() == sdk::local_controller->m_iTeamNum()
    		|| !controller->m_bPawnIsAlive()) continue;
     
    	C_BasePlayerPawn* pawn = interfaces::g_game_resouce->entity_system->Get<C_BasePlayerPawn>(controller->m_hPawn());
    	if (!pawn || pawn == sdk::local_pawn) { continue; }
    }
```

```

```
