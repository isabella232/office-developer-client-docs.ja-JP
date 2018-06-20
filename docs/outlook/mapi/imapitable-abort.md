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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800820"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**適用されます**: Outlook 
  
テーブルの現在進行中のすべての非同期操作を停止します。
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Parameters

なし
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> 1 つまたは複数の非同期操作が中止されました。
    
MAPI_E_UNABLE_TO_ABORT 
  
> 非同期操作の進行中および停止することはできませんまたはが既に完了しました。
    
## <a name="remarks"></a>備考

**IMAPITable::Abort**メソッドは、実行中である非同期操作を停止します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

非同期操作が行われているについては、 [IMAPITable::GetStatus](imapitable-getstatus.md)メソッドを呼び出します。 
  
**中止**すると、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドの呼び出しの処理が停止し、テーブルの状態は、**アボート**の呼び出しが処理されるときにあります。 
  
**中止**すると、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドの呼び出しの処理が停止し、テーブルの並べ替え順序に影響がないと、 **SortTable**の呼び出しの前に、と同じままになります。 
  
## <a name="see-also"></a>関連項目



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

