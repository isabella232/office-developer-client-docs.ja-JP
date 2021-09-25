---
title: Outlook がメッセージのヘッダーのみをダウンロードしたかどうかを判別する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: acc96bb9-1592-c480-53ee-1325f65297e1
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 04770b2838941239219637a75435fcdd586dca55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551437"
---
# <a name="determine-if-outlook-downloaded-only-the-header-of-a-message"></a>Outlook がメッセージのヘッダーのみをダウンロードしたかどうかを判別する

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、Visual C++ で、名前の付いた[PidLidHeaderItem Canonical プロパティ](pidlidheaderitem-canonical-property.md)を使用して、Microsoft Outlook 2013 がメッセージのヘッダーまたはヘッダーとメッセージの本文のみをダウンロードしたかどうかを判断するコード サンプルを示します。 
  
```cpp
BOOL bIsHeader(LPMESSAGE lpMessage) 
{ 
    HRESULT         hRes = S_OK; 
    BOOL            bRet = false; 
    ULONG    ulVal = 0; 
    LPSPropValue    lpPropVal = NULL; 
    LPSPropTagArray lpNamedPropTag = NULL; 
    MAPINAMEID      NamedID = {0}; 
    LPMAPINAMEID    lpNamedID = NULL; 
 
    NamedID.lpguid = (LPGUID) &PSETID_Common; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidHeaderItem; 
    lpNamedID = &NamedID; 
    hRes = lpMessage->GetIDsFromNames(1, &lpNamedID, NULL, &lpNamedPropTag); 
 
    if (lpNamedPropTag && 1 == lpNamedPropTag->cValues) 
    { 
lpNamedPropTag->aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTag->aulPropTag[0], PT_LONG); 
 
//Get the value of the property. 
hRes = lpMessage->GetProps(lpNamedPropTag, 0, &ulVal, &lpPropVal); 
if (lpPropVal && 1 == ulVal && PT_LONG == PROP_TYPE(lpPropVal->ulPropTag) && lpPropVal->Value.ul) 
{ 
    bRet = true; 
} 
    } 
 
    MAPIFreeBuffer(lpPropVal); 
    MAPIFreeBuffer(lpNamedPropTag); 
    return bRet; 
}

```


