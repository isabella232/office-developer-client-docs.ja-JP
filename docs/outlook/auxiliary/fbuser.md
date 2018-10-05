---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: 利用可能な空き時間情報データがない可能性がありますは、ユーザーを識別します。
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387903"
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
  
> [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops)インターフェイスによって表される、メール ユーザーのエントリ ID の長さ。 
    
_m_lpEid_
  
> **IMailUser**インターフェイスによって表される、メール ユーザーのエントリ ID です。 
    
_m_ulReserved_
  
> このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。
    
_m_pwszReserved_
  
> このパラメーターは、Outlook の内部使用に予約されている、サポートされていません。
    
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

