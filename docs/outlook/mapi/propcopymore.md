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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404471"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つのプロパティ値をソースの場所からコピー先の場所にコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>パラメーター

 _lpSPropValueDest_
  
> [out]コピーされたプロパティ値を定義する [SPropValue](spropvalue.md) 構造体をこの関数が書き込む場所へのポインター。 
    
 _lpSPropValueSrc_
  
> [in]コピーする [プロパティ値を含む SPropValue](spropvalue.md) 構造体へのポインター。 
    
 _lpfAllocMore_
  
> [in]コピー先の場所がコピーするプロパティを保持するのに十分な大きさではない場合に、追加のメモリを割り当てるのに使用する [MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。 
    
 _lpvObject_
  
> [in] **MAPIAllocateMore** が必要に応じて領域を割り当てるオブジェクトへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> 単一のプロパティ値が正常にコピーされました。
    
MAPI_E_NO_SUPPORT
  
> 不明なプロパティの種類が検出されました。
    
## <a name="remarks"></a>注釈

クライアント アプリケーションまたはサービス プロバイダーは **PropCopyMore** 関数を使用して、他の場所でプロパティを使用するために解放されるテーブルからプロパティをコピーできます。 
  
 **PropCopyMore は** 、コピーされるプロパティ値が [sPropValue](spropvalue.md) 構造体に収まらない PT_STRING8 などの型の場合を指定しない限り、メモリを割り当てる必要があります。 これらの大きなプロパティの場合、関数は、ポインターが _lpfAllocMore_ パラメーターで渡される [MAPIAllocateMore](mapiallocatemore.md)関数を使用してメモリを割り当てる。 
  
**PropCopyMore** フラグメント メモリの不当な使用。代わりに [ScCopyProps 関数の使用](sccopyprops.md)を検討してください。 
  

