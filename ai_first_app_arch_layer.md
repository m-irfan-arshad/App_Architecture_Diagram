---
config:
  layout: dagre
  theme: neo
---
flowchart TB
 subgraph Layer1["Cloud Layer"]
        AI["AI ServicesMachine Learning ModelsNLP Processing"]
        Backend["Backend ServicesAPI GatewayData Processing"]
        Storage["Cloud StorageUser DataAI Model Storage"]
  end
 subgraph Core["Core Components"]
        AIInt["AI IntegrationOn-device MLAI Capabilities"]
        StateM["State ManagementData Flow"]
        APIInt["API IntegrationCloud Sync"]
        Sec["SecurityEncryptionAuthentication"]
  end
 subgraph UI["User Interface"]
        IntUI["Intelligent UIAdaptive InterfacesPersonalizationContext Awareness"]
        UX["User ExperienceVoice InteractionsVisual RecognitionPredictive Features"]
        DeviceAI["On-device AITensorFlow Lite/Core MLEdge Inference"]
  end
 subgraph Layer2["Mobile Application Layer"]
        Core
        UI
  end
 subgraph Layer3["Device Layer"]
        Mobile["Mobile DeviceiOS / Android"]
  end
    Layer1 L_Layer1_Layer2_0@== Cloud APIs ==> Layer2
    AI L_AI_AIInt_0@== Models & Inference ==> AIInt
    Backend L_Backend_Core_0@== Data & Services ==> Core
    Storage L_Storage_APIInt_0@== Sync ==> APIInt
    Core == State & Data ==> UI
    AIInt == AI Features ==> IntUI
    AIInt == ML Processing ==> DeviceAI
    Layer2 == Native App ==> Layer3
    style Layer1 stroke:#2962FF,stroke-width:2px
    style Layer2 fill:transparent,stroke:#2962FF,stroke-width:2px
    style Layer3 fill:transparent,stroke:#4dabf7,stroke-width:2px, wight:500ps
    linkStyle 3 stroke:#000000,fill:none
    L_Layer1_Layer2_0@{ animation: none } 
    L_AI_AIInt_0@{ animation: none } 
    L_Backend_Core_0@{ animation: none } 
    L_Storage_APIInt_0@{ animation: none }
