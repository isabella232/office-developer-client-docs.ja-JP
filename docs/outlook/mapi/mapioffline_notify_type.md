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
ms.openlocfilehash: e7120b843eae8df70cb2c4f9cbf581dcf0e09c11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566888"
---
# <a name="mapiofflinenotifytype"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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



[オフライン状態 API について](about-the-offline-state-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

