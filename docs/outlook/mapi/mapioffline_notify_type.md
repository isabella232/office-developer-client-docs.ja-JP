---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 468dfd634c4aaf18b019d06975ec9066c9d5f7a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801512"
---
# <a name="mapiofflinenotifytype"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**適用されます**: Outlook 
  
通知の MAPIOFFLINE_NOTIFY_TYPE では、接続状態の変更を実行しようとしていますが行われて、または完了した場合を識別します。 
  
## <a name="quick-info"></a>クイック ヒント

**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を参照してください。 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a>関連項目



[オフラインの状態の API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

