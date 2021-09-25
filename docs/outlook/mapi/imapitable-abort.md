---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bc55f579e7d161d9899d29e5c8239db347980c53
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630685"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの現在進行中の非同期操作を停止します。
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 1 つ以上の非同期操作が停止しました。
    
MAPI_E_UNABLE_TO_ABORT 
  
> 非同期操作は進行中で、停止できないか、既に完了しています。
    
## <a name="remarks"></a>注釈

**IMAPITable::Abort** メソッドは、現在進行中の非同期操作を停止します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

非同期操作が進行中の場合は [、IMAPITable::GetStatus メソッドを呼び出](imapitable-getstatus.md) します。 
  
Abort **が** [IMAPITable::Restrict](imapitable-restrict.md)メソッドへの呼び出しの処理を停止すると、テーブルの状態は Abort 呼び出しが処理された時点と同じになります。 
  
Abort **が** [IMAPITable::SortTable](imapitable-sorttable.md) メソッドの呼び出しの処理を停止すると、テーブルの並べ替え順序は影響を受けず **、SortTable** 呼び出しの前と同じままです。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

