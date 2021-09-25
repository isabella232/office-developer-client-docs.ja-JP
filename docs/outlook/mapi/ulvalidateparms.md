---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d111c6a0e51f3487014a411b6b7ebf4e3d588744
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578418"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、クライアント アプリケーションがサービス プロバイダーと MAPI に渡したパラメーターを確認します。 
  
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
  
> [in]列挙で検証するメソッドを指定します。 
    
 _First_
  
> [in]スタックの最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> エラーが発生すると、操作が完了しきれなかった。
    
## <a name="remarks"></a>注釈

MAPI とサービス プロバイダーの間で渡されるパラメーターは正しいと見なされ [、CheckParms](checkparms.md) マクロを使用してデバッグ検証のみを行います。 プロバイダーは、クライアント アプリケーションによって渡されるパラメーターを確認する必要がありますが、クライアントは MAPI パラメーターとプロバイダー パラメーターが正しいと想定する必要があります。 戻り値 **をHR_FAILED** するには、次のマクロを使用します。 
  
**UlValidateParms** マクロの呼び出し方法は、呼び出し元のコードが C か C++かによって異なります。 このマクロは、HRESULT 値の代わりに ULONG を返す少数の **IUnknown** メソッドおよび MAPI メソッドのパラメーターを検証するために使用されます。 [ValidateParms マクロは](validateparms.md) 、他のすべてのユーザーに対して機能します。 
  

