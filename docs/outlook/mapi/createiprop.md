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
  
プロパティデータオブジェクト ( [ipropdata](ipropdataimapiprop.md)オブジェクト) を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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

 _lpinterface_
  
> 順番プロパティデータオブジェクトのインターフェイス識別子 (IID) へのポインター。 有効なインターフェイス識別子は IID_IMAPIPropData です。 _lpinterface_パラメーターで NULL を渡すと、 _lpppropdata_パラメーターで返される property data オブジェクトが、プロパティデータオブジェクトの標準インターフェイスにキャストされることもあります。 
    
 _lpAllocateBuffer_
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> 順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpvreserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _lpppropdata_
  
> 読み上げ返されたプロパティデータオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> 要求されたインターフェイスは、このオブジェクトではサポートされていません。
    
## <a name="remarks"></a>注釈

_lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_の入力パラメーターは、それぞれ、 [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)関数を指しています。 **createiprop**を呼び出すクライアントアプリケーションは、という名前の MAPI 関数へのポインターをパスに渡します。サービスプロバイダーは、初期化呼び出しで受け取った、または[imapiallocルーチン](imapisupport-getmemallocroutines.md)メソッドへの呼び出しによって取得したこれらの関数へのポインターを渡します。 
  

