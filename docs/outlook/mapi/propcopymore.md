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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 750d8b8d50acb9cf7340e6553062412667398665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803693"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**適用されます**: Outlook 
  
1 つのプロパティの値を元の場所から先の場所にコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>Parameters

 _lpSPropValueDest_
  
> [out]書き込みます、 [SPropValue](spropvalue.md)構造体がコピーされたプロパティ値を定義する場所へのポインター。 
    
 _lpSPropValueSrc_
  
> [in]コピーするプロパティの値を含む[SPropValue](spropvalue.md)構造体へのポインター。 
    
 _lpfAllocMore_
  
> [in]先にコピーするプロパティを保持するのに十分な大きさがない場合、追加のメモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpvObject_
  
> [in]対象の**MAPIAllocateMore**は領域を割り当てる必要がある場合、オブジェクトへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> 1 つのプロパティの値は、正常にコピーされました。
    
MAPI_E_NO_SUPPORT
  
> 不明なプロパティの種類が発生しました。
    
## <a name="remarks"></a>備考

クライアント アプリケーションまたはサービス プロバイダーは、それを別の場所で使用するために解放しようとしているテーブルのプロパティをコピーするのには、 **PropCopyMore**関数を使用することができます。 
  
 **PropCopyMore**は PT_STRING8、 [SPropValue](spropvalue.md)構造に適合しないなどの型がプロパティの値をコピーしない限り、メモリを割り当てる必要はありません。 、これらの大規模なプロパティは、関数は、 _lpfAllocMore_パラメーターで、ポインターが渡されます[MAPIAllocateMore](mapiallocatemore.md)関数を使用してメモリを割り当てます。 
  
**PropCopyMore**の injudicious の使用にはメモリがフラグメント化します。代わりに[ScCopyProps](sccopyprops.md)関数を使用してください。 
  

