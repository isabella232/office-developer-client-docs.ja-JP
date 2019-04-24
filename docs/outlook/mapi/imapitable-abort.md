---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328952"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルに対して現在進行中のすべての非同期操作を停止します。
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 1つ以上の非同期操作が停止されています。
    
MAPI_E_UNABLE_TO_ABORT 
  
> 非同期操作が進行中で、停止できないか、既に完了しています。
    
## <a name="remarks"></a>解説

**IMAPITable:: Abort**メソッドは、現在進行中のすべての非同期操作を停止します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

非同期操作が進行中かどうかを確認するには、 [IMAPITable:: GetStatus](imapitable-getstatus.md)メソッドを呼び出します。 
  
**中止**すると、 [IMAPITable:: Restrict](imapitable-restrict.md)メソッドへの呼び出しの処理が停止した場合、テーブルの状態は**abort**呼び出しが処理された時点の状態になります。 
  
**中止**すると、 [IMAPITable:: sorttable](imapitable-sorttable.md)メソッドへの呼び出しの処理が停止した場合、テーブルの並べ替え順序は影響を受けず、 **sorttable**呼び出しの前と同じ状態になります。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

