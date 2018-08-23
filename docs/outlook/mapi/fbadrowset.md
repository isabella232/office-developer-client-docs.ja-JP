---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e86e9fbf4901b5944775886f38db1ba12c4b122d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590961"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルの行のセットに含まれるすべてのテーブルの行を検証します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>パラメーター

 _lpRowSet_
  
> [in][SRowSet](srowset.md)構造体を検証する設定の行を識別するへのポインター。 ポインターが NULL の場合は、構造が正しくありません。 
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定した行セットの行が正しくないか、またはそれ自体を設定した行が有効ではありません。 
    
FALSE 
  
> 指定した行セットの行と行は設定自体は、すべてに有効です。
    
## <a name="see-also"></a>関連項目



[FBadRow](fbadrow.md)

