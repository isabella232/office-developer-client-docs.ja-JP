---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800805"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**適用対象**: Outlook 
  
[送受信] ダイアログ ボックスの状態を更新します。 ストア プロバイダーは、定期的にこの関数を呼び出します。
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>パラメーター

 **pwczsProgress**
  
> 現在進行中のステップを表示する文字列へのポインター。 進捗状況を更新するのには NULL を指定できます。
    
 **ulIndex**
  
> 進行中の現在の位置。
    
 **ulIndexMax**
  
> 完全な進捗状況を示すインデックス。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

