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
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800819"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**適用対象**: Outlook 
  
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

