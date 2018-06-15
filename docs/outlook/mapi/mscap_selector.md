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
ms.openlocfilehash: 420b2661e766ecf97a5e9e488e9c18f29cd91329
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19801645"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

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
    

