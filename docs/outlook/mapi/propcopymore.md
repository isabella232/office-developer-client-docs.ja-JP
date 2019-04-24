---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328554"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つのプロパティ値をソースの場所から移動先の場所にコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>パラメーター

 _lpspropvaluedest_
  
> 読み上げこの関数がコピーされたプロパティ値を定義する[spropvalue](spropvalue.md)構造を書き込む場所へのポインター。 
    
 _lpspropて rc_
  
> 順番コピーするプロパティ値を含む[spropvalue](spropvalue.md)構造体へのポインター。 
    
 _lpfAllocMore_
  
> 順番コピーするプロパティを保持するには、コピー先の場所が十分でない場合に、追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpvobject_
  
> 順番**MAPIAllocateMore**が必要に応じてスペースを割り当てるオブジェクトへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 単一のプロパティ値が正常にコピーされました。
    
MAPI_E_NO_SUPPORT
  
> 不明なプロパティの種類が検出されました。
    
## <a name="remarks"></a>解説

クライアントアプリケーションまたはサービスプロバイダーは、 **propcopymore**関数を使用して、別の場所で使用するために解放されることになるテーブルからプロパティをコピーできます。 
  
 コピーされたプロパティ値が PT_STRING8 など、 [spropvalue](spropvalue.md)構造に適合しない場合を除いて、 **propcopymore**はメモリを割り当てる必要はありません。 このような大きなプロパティの場合、関数は、ポインターが_lpfAllocMore_パラメータで渡される[MAPIAllocateMore](mapiallocatemore.md)関数を使用してメモリを割り当てます。 
  
injudicious use **propcopymore**の断片メモリ。代わりに、 [sccopyprops](sccopyprops.md)関数の使用を検討してください。 
  

