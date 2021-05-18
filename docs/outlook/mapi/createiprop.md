---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406809"
---
# <a name="createiprop"></a>CreateIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ データ オブジェクト (つまり [、IPropData](ipropdataimapiprop.md) オブジェクト) を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a>パラメーター

 _lpInterface_
  
> [in]プロパティ データ オブジェクトのインターフェイス識別子 (IID) へのポインター。 有効なインターフェイス識別子はIID_IMAPIPropData。 _lpInterface_ パラメーターに NULL を渡した場合 _、lppPropData_ パラメーターで返されるプロパティ データ オブジェクトも、プロパティ データ オブジェクトの標準インターフェイスにキャストされます。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。 
    
 _lpvReserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _lppPropData_
  
> [out]返されるプロパティ データ オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> 要求されたインターフェイスは、このオブジェクトではサポートされていません。
    
## <a name="remarks"></a>注釈

_lpAllocateBuffer_ _、lpAllocateMore、lpFreeBuffer_ 入力パラメーターは [、MAPIAllocateBuffer、MAPIAllocateMore、MAPIFreeBuffer](mapiallocatebuffer.md)関数をそれぞれ指します。  [](mapiallocatemore.md) [](mapifreebuffer.md) **CreateIProp を呼び出すクライアント** アプリケーションは、という名前の MAPI 関数へのポインターを渡します。サービス プロバイダーは、初期化呼び出しで受信した、[または IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドへの呼び出しで取得されたこれらの関数へのポインターを渡します。 
  

