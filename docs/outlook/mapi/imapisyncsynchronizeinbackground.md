---
title: IMAPISync SynchronizeInBackground
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
ms.openlocfilehash: ee6fe07df894213331ab51f9abaa4008247dac07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568778"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 同期を開始します。 このメソッドは、Microsoft Outlook 2010 と Microsoft Outlook 2013 で呼び出され、メッセージ ストア プロバイダーによって実装されています。 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>パラメーター

 _psibpb_
  
> プロバイダーと同期するを通知し、同期中に使用できるインターフェイスにアクセスします。 それは、 [MAPISIB](mapisib.md)構造です。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

