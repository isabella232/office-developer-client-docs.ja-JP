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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a22f7628b306707474e4ffb6fdf4525e00bf0771
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804235"
---
# <a name="validateparms"></a>ValidateParms

  
  
**適用されます**: Outlook 
  
パラメーターのクライアント アプリケーションがサービス プロバイダーに渡されますが確認するのには内部の関数を呼び出します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parameters

 _」方法_
  
> [in]確認する方法を列挙型を指定します。 
    
 _First/先頭のレコード_
  
> [in]スタック上の最初の引数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> すべてのパラメーターは、有効です。 
    
MAPI_E_CALL_FAILED 
  
> 1 つまたは複数のパラメーターが有効ではありません。
    
## <a name="remarks"></a>備考

MAPI とサービスの間で渡されるパラメーターを正しくし、 [CheckParms](checkparms.md)マクロのデバッグ検証のみを行うプロバイダーと見なされます。 プロバイダーは、クライアント アプリケーションによって渡されるすべてのパラメーターを確認する必要がありますが、クライアントが MAPI およびプロバイダーのパラメーターが正しいことを想定する必要があります。 戻り値をテストするのにには、 **HR_FAILED**マクロを使用します。 
  
 **ValidateParms**は、呼び出し元のコードが C または C++ のどちらであるかに応じて異なる方法で呼び出されます。 C++ では、各メソッドの呼び出しに、c 言語では明示的になり、オブジェクトのアドレスを_この_と呼ばれる暗黙のパラメーターを渡します。 _」方法_では、最初のパラメーターを使用して、列挙子インターフェイスとメソッドの検証対象からは、スタックで見つけられるには、どのようなパラメーターを示します。 2 番目のパラメーターは、C および C++ では異なります。 C++ では、_最初_と呼びますが最初のパラメーターを検証するメソッド。 C 言語、 _ppThis_の 2 番目のパラメーターは、常にオブジェクト ポインターであるメソッドの最初のパラメーターのアドレスです。 どちらの場合も、2 番目のパラメーター、メソッドのパラメーター リストの先頭のアドレスでは、 _」方法_に基づく、スタックの下に移動し、パラメーターを検証します。 
  
**IMAPITable**や**IMAPIProp**などの一般的なインターフェイスを実装するプロバイダーでは、すべてのプロバイダー間での整合性の確認を行うために、 **ValidateParms**関数を使用してパラメーターを常に確認しています。 追加のパラメーターの検証関数は、必要に応じてその代わりに使用するいくつかの複雑なパラメーター型の定義されています。 次の関数のリファレンス トピックを参照してください。 
  
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
    
継承されたメソッドは、継承元となるインターフェイスとして同じパラメーターの検証を使用します。 **IMessage**および**IMAPIProp**をチェックするパラメーターは、同じにする必要があります。 
  
## <a name="see-also"></a>関連項目



[UlValidateParms](ulvalidateparms.md)

