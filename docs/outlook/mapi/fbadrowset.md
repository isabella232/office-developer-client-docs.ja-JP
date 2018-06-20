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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800067"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _lpRowSet_
  
> [in][SRowSet](srowset.md)構造体を検証する設定の行を識別するへのポインター。 ポインターが NULL の場合は、構造が正しくありません。 
    
## <a name="return-value"></a>�߂�l

TRUE 
  
> 指定した行セットの行が正しくないか、またはそれ自体を設定した行が有効ではありません。 
    
FALSE 
  
> 指定した行セットの行と行は設定自体は、すべてに有効です。
    
## <a name="see-also"></a>関連項目



[FBadRow](fbadrow.md)

