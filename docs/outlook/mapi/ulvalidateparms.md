---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419612"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、クライアントアプリケーションがサービスプロバイダーと MAPI に渡されたことを確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>パラメーター

 _eMethod_
  
> 順番検証するメソッドを列挙で指定します。 
    
 _First_
  
> 順番スタック上の最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> エラーが発生したため、操作を完了できませんでした。
    
## <a name="remarks"></a>注釈

MAPI プロバイダーとサービスプロバイダー間で渡されるパラメーターは正しいと見なされ、 [checkparms](checkparms.md)マクロを使用してのみ、デバッグ検証を行います。 プロバイダーは、クライアントアプリケーションによって渡されたすべてのパラメーターをチェックする必要がありますが、クライアントは MAPI および provider パラメーターが正しいと想定する必要があります。 **HR_FAILED**マクロを使用して、戻り値をテストします。 
  
**ulvalidateparms**マクロは、呼び出し元のコードが C または C++ のどちらであるかによって、異なる方法で呼び出されます。 このマクロは、HRESULT 値ではなく ULONG を返すいくつかの**IUnknown**および MAPI メソッドのパラメーターを検証するために使用されます。[validateparms](validateparms.md)マクロは、他のすべてのユーザーに対して動作します。 
  

