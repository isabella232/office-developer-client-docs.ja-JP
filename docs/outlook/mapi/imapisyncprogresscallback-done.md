---
title: imapisync進行 scallbackdone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341273"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 同期が完了したことを Microsoft Outlook に通知します。 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>パラメーター

 **h月間 addoneevent**
  
> Microsoft Outlook がハンドルを閉じることができるようにするイベントを返します。 NULL でもかまいません。
    
 **hResult**
  
> 進行状況の最終状態を示す HRESULT。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

