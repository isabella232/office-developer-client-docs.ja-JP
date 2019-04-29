---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406340"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティセット内の指定されたプロパティを検索します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>パラメーター

 _rgprop_
  
> 順番検索するプロパティを定義する[spropvalue](spropvalue.md)構造の配列です。 
    
 _cprop_
  
> 順番_rgprop_パラメーターによって示されるプロパティセット内のプロパティの数。 
    
 _ulPropTag_
  
> 順番_rgprop_パラメーターによって示されるプロパティセット内で検索するプロパティのプロパティタグ。 
    
## <a name="return-value"></a>戻り値

 **ppropfindprop**は、入力プロパティタグに一致するプロパティを定義する[spropvalue](spropvalue.md)構造体を返します。一致しない場合は NULL になります。 
  
## <a name="remarks"></a>注釈

指定したプロパティタグが PT_UNSPECIFIED 型のプロパティを示している場合、 **ppropfindprop**関数は、タグ内のプロパティ識別子に対してのみ一致を検出します。 それ以外の場合は、プロパティの型を含む property タグ全体の一致を検索し、識別されたプロパティを返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContentsTableListCtrl:: builddataitem  <br/> |mfcmapi は、 **ppropfindprop**メソッドを使用して、リストに追加されているプロパティセット内のプロパティを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

