---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436806"
---
# <a name="validateparms"></a>ValidateParms

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、クライアントアプリケーションがサービスプロバイダーに渡されたパラメーターを確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT ValidateParms(
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
  
> すべてのパラメーターが有効です。 
    
MAPI_E_CALL_FAILED 
  
> 1つ以上のパラメーターが無効です。
    
## <a name="remarks"></a>注釈

MAPI プロバイダーとサービスプロバイダー間で渡されるパラメーターは正しいと見なされ、 [checkparms](checkparms.md)マクロを使用してのみ、デバッグ検証を行います。 プロバイダーは、クライアントアプリケーションによって渡されたすべてのパラメーターをチェックする必要がありますが、クライアントは MAPI および provider パラメーターが正しいと想定する必要があります。 **HR_FAILED**マクロを使用して、戻り値をテストします。 
  
 **validateparms**は、呼び出し元のコードが C または C++ のどちらであるかによって、異なる呼び出しを行います。 C++ は、 _this_という暗黙的なパラメーターを各メソッド呼び出しに渡します。これは、C で明示的になり、オブジェクトのアドレスです。 最初のパラメーター _eMethod_は、インターフェイスおよび検証されたメソッドからの列挙子です。スタック上で検索するパラメーターを示します。 2番目のパラメーターは、C および C++ とは異なります。 C++ では、_最初_に呼び出され、検証されるメソッドの最初のパラメーターです。 C 言語の2番目のパラメーター _ppthis_は、メソッドに対する最初のパラメーターのアドレスで、常にオブジェクトポインターです。 どちらの場合も、2番目のパラメーターによって、メソッドのパラメーターリストの先頭のアドレスが指定され、 _eMethod_に基づいてスタックが下に移動され、パラメーターが検証されます。 
  
**IMAPITable**や**imapiprop**などの一般的なインターフェイスを実装するプロバイダーは、すべてのプロバイダー間で一貫性を確保するために、必ず**validateparms**関数を使用してパラメーターをチェックする必要があります。 その代わりに使用されるように、いくつかの複雑なパラメーターの検証関数が定義されています。 次の関数については、リファレンストピックを参照してください。 
  
- [FBadColumnSet](fbadcolumnset.md)
    
- [FBadEntryList](fbadentrylist.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRglpszW](fbadrglpszw.md)
    
- [FBadRow](fbadrow.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
継承されたメソッドは、継承元のインターフェイスと同じパラメーター検証を使用します。 たとえば、 **IMessage**と**imapiprop**をチェックするパラメーターは同じである必要があります。 
  
## <a name="see-also"></a>関連項目



[UlValidateParms](ulvalidateparms.md)

