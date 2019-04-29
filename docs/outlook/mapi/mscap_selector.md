---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417204"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストアに対して返す機能を指定します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a>メンバー

 *MSCAP_SEL_RESERVED1* 
  
> このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。 
    
 *MSCAP_SEL_RESERVED2* 
  
> このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。 
    
 *MSCAP_SEL_FOLDER* 
  
> ストア上のフォルダーのサポートに関する機能。
    
 *MSCAP_SEL_RESERVED3* 
  
> このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。 
    
 *MSCAP_SEL_RESTRICTION* 
  
> ストアに対する制限のサポートに関する機能。
    

