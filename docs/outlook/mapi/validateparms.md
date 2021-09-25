---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d767eae393e31a2c55dbafe0a608bbbc121e60c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623888"
---
# <a name="validateparms"></a>ValidateParms

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、クライアント アプリケーションがサービス プロバイダーに渡したパラメーターを確認します。 
  
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
  
> [in]列挙で検証するメソッドを指定します。 
    
 _First_
  
> [in]スタックの最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> すべてのパラメーターが有効です。 
    
MAPI_E_CALL_FAILED 
  
> 1 つ以上のパラメーターが無効です。
    
## <a name="remarks"></a>注釈

MAPI とサービス プロバイダーの間で渡されるパラメーターは正しいと見なされ [、CheckParms](checkparms.md) マクロを使用してデバッグ検証のみを行います。 プロバイダーは、クライアント アプリケーションによって渡されるパラメーターを確認する必要がありますが、クライアントは MAPI パラメーターとプロバイダー パラメーターが正しいと想定する必要があります。 戻り値 **をHR_FAILED** するには、次のマクロを使用します。 
  
 **ValidateParms は** 、呼び出し元のコードが C か C++ かによって呼び出し方法が異なります。 C++ は、これを呼び出す暗黙的なパラメーターを各メソッド呼び出しに渡します。これは C では明示的になり、オブジェクトのアドレスです。 最初のパラメーター  _eMethod_ は、検証されるインターフェイスとメソッドから作成された列挙子であり、スタック上で検索する必要があるパラメーターを示します。 2 番目のパラメーターは、C と C++ では異なります。 C++ では First  _と呼び_、検証されるメソッドの最初のパラメーターです。 C 言語の 2 番目のパラメーター  _ppThis_ は、常にオブジェクト ポインターであるメソッドの最初のパラメーターのアドレスです。 どちらの場合も、2 番目のパラメーターはメソッドのパラメーター リストの先頭のアドレスを指定し  _、eMethod_ に基づいてスタックを下に移動し、パラメーターを検証します。 
  
**IMAPITable** や **IMAPIProp** などの一般的なインターフェイスを実装するプロバイダーは、すべてのプロバイダー間で一貫性を確保するために **、ValidateParms** 関数を使用してパラメーターを常にチェックする必要があります。 必要に応じて、一部の複雑なパラメーター型を使用するために、追加のパラメーター検証関数が定義されています。 以下の機能については、リファレンス トピックを参照してください。 
  
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
    
継承されたメソッドは、継承元のインターフェイスと同じパラメーター検証を使用します。 たとえば **、IMessage** と **IMAPIProp** のパラメーター チェックは同じにする必要があります。 
  
## <a name="see-also"></a>関連項目



[UlValidateParms](ulvalidateparms.md)

