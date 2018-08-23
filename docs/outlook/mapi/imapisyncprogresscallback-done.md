---
title: IMAPISyncProgressCallbackDone
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cdd3db3f3779c2078b90352e19f8da6b29cffb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573209"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 Microsoft Outlook に通知の同期が完了しています。 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>パラメーター

 **hThreadDoneEvent**
  
> ハンドルを閉じるための Microsoft Outlook を許可するのに渡されるイベントです。 NULL にすることができます。
    
 **hResult**
  
> 進行状況の最終的な状態を示す HRESULT。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

