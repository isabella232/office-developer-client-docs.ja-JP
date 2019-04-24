---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: 空き時間情報を利用できるかどうかが不明なユーザーを識別します。
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317662"
---
# <a name="fbuser"></a>FBUser

空き時間情報を利用できるかどうかが不明なユーザーを識別します。
  
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

## <a name="members"></a>メンバー

_m_cbEid_
  
> [imailuser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops)インターフェイスで表されるメールユーザーのエントリ ID の長さ。 
    
_m_lpEid_
  
> **imailuser**インターフェイスで表されるメールユーザーのエントリ ID。 
    
_m_ulReserved_
  
> このパラメーターは、Outlook の内部使用のために予約されており、サポートされていません。
    
_m_pwszReserved_
  
> このパラメーターは、Outlook の内部使用のために予約されており、サポートされていません。
    
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

