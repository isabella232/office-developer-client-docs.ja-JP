---
title: imapisyncprogress scallbackprogress
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341259"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信/受信ダイアログの状態を更新します。 ストアプロバイダーは、この関数を定期的に呼び出します。
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>パラメーター

 **pwczsProgress**
  
> 現在の進行状況のステップを表示する文字列へのポインター。 進捗状況を更新する場合は、NULL にすることができます。
    
 **ulindex**
  
> 現在進行中の位置。
    
 **ulindexmax**
  
> 完全な進捗状況を示すインデックス。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

