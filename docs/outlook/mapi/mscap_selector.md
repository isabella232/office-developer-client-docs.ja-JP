---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588126"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ストアを取得する機能を指定します。
  
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

## <a name="members"></a>Members

 *MSCAP_SEL_RESERVED1* 
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
 *MSCAP_SEL_RESERVED2* 
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
 *MSCAP_SEL_FOLDER* 
  
> ストアにフォルダーをサポートする機能です。
    
 *MSCAP_SEL_RESERVED3* 
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
 *MSCAP_SEL_RESTRICTION* 
  
> ストアの制限をサポートする機能です。
    

