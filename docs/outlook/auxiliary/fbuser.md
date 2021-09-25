---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: 空き時間情報データを使用できるユーザーまたは使用できない可能性があるユーザーを識別します。
ms.openlocfilehash: e3c67d8cf4e858fa6b5bdde7bb1714c5caacb484
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568041"
---
# <a name="fbuser"></a>FBUser

空き時間情報データを使用できるユーザーまたは使用できない可能性があるユーザーを識別します。
  
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
  
> [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops)インターフェイスで表されるメール ユーザーのエントリ ID の長さ。 
    
_m_lpEid_
  
> IMailUser インターフェイスで表されるメール ユーザー **のエントリ ID。** 
    
_m_ulReserved_
  
> このパラメーターは、内部Outlook使用するために予約され、サポートされていません。
    
_m_pwszReserved_
  
> このパラメーターは、内部Outlook使用するために予約され、サポートされていません。
    
## <a name="see-also"></a>関連項目

- [空き時間情報 API について](about-the-free-busy-api.md)  
- [IFreeBusySupport](ifreebusysupport.md)

