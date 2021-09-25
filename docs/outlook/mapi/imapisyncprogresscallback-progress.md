---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0f01f495372122c2c2f8b2e5d1242d7a1898f62f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592341"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[送受信] ダイアログの状態を更新します。 ストア プロバイダーは定期的にこの関数を呼び出します。
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>パラメーター

 **pwczsProgresss**
  
> 現在の進行状況の手順を表示する文字列へのポインター。 進行状況を更新するには NULL を指定できます。
    
 **ulIndex**
  
> 進行中の現在の位置。
    
 **ulIndexMax**
  
> 完全な進行状況を示すインデックス。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

