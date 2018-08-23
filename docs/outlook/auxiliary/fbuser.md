---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: 利用可能な空き時間情報データがない可能性がありますは、ユーザーを識別します。
ms.openlocfilehash: e83689e28f5fb6e1eae28d760bb57f5ad3796f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799307"
---
# <a name="fbuser"></a>FBUser

利用可能な空き時間情報データがない可能性がありますは、ユーザーを識別します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a>Members

_m_cbEid_
  
> [IMailUser](http://msdn.microsoft.com/library/wab._wab_IMailUser%28Office.15%29.aspx)インターフェイスによって表される、メール ユーザーのエントリ ID の長さ。 
    
_m_lpEid_
  
> **IMailUser**インターフェイスによって表される、メール ユーザーのエントリ ID です。 
    
_m_ulReserved_
  
> このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。
    
_m_pwszReserved_
  
> このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。
    
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

