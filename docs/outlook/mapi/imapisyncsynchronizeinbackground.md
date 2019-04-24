---
title: imapisync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341371"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 同期を開始します。 このメソッドは、microsoft outlook 2010 および microsoft outlook 2013 によって呼び出され、メッセージストアプロバイダーによって実装されます。 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>パラメーター

 _psibpb_
  
> 同期される対象をプロバイダーに通知し、同期中に使用できるインターフェイスへのアクセスを提供します。 [MAPISIB](mapisib.md)構造です。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

