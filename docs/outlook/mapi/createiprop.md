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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 906dc4a24b994e079a977808c3f501aaaea9d84f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799859"
---
# <a name="createiprop"></a>CreateIProp

  
  
**適用されます**: Outlook 
  
プロパティのデータ オブジェクトは、 [IPropData](ipropdataimapiprop.md)オブジェクトを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in]インターフェイス識別子 (IID) のプロパティのデータ オブジェクトへのポインター。 有効なインタ フェース識別子は、IID_IMAPIPropData です。 プロパティのデータ オブジェクトの標準的なインターフェイスにキャストするのには_lppPropData_パラメーターで返されるプロパティのデータ オブジェクトは、 _lpInterface_パラメーターに NULL を渡すことも。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpvReserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _lppPropData_
  
> [out]返されるプロパティのデータ オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> このオブジェクトには、要求されたインターフェイスはサポートされていません。
    
## <a name="remarks"></a>備考

_LpAllocateBuffer_、 _lpAllocateMore_、および_lpFreeBuffer_の入力パラメーターは、それぞれ[MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)関数では、] をポイントします。 **CreateIProp**を呼び出すクライアント アプリケーションが MAPI の関数を同じ名前でポインターを渡しますサービス プロバイダーは、これらの関数は、初期化の呼び出しで受信した、 [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドの呼び出しで取得したポインターを渡します。 
  

