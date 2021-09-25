---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d97c88ee27fbe0b68c7495657c77fa2ca4734e81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604762"
---
# <a name="mapioffline_notify_type"></a>MAPIOFFLINE_NOTIFY_TYPE

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知MAPIOFFLINE_NOTIFY_TYPEは、接続状態の変更が行うのか、起こっているのか、完了したのか、を識別します。 
  
## <a name="quick-info"></a>クイック ヒント

**[「IMAPIOfflineNotify」を参照してください](imapiofflinenotifyiunknown.md)**。 
  
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

