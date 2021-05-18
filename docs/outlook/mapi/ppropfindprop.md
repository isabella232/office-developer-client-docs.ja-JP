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
  
プロパティ セット内の指定されたプロパティを検索します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>パラメーター

 _rgprop_
  
> [in]検索する [プロパティを定義する SPropValue](spropvalue.md) 構造体の配列。 
    
 _cprop_
  
> [in]  _rgprop_ パラメーターで示されるプロパティ セット内のプロパティの数。 
    
 _ulPropTag_
  
> [in]  _rgprop_ パラメーターで示されるプロパティ セット内で検索するプロパティのプロパティ タグ。 
    
## <a name="return-value"></a>戻り値

 **PpropFindProp** は、入力プロパティ タグに一致するプロパティを定義する [SPropValue](spropvalue.md) 構造体を返します。一致しない場合は NULL を返します。 
  
## <a name="remarks"></a>注釈

指定されたプロパティ タグが PT_UNSPECIFIED 型のプロパティを示す場合 **、PpropFindProp** 関数はタグ内のプロパティ識別子の一致のみを検索します。 それ以外の場合は、プロパティの種類を含むプロパティ タグ全体の一致を検索し、識別されたプロパティを返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI は **PpropFindProp** メソッドを使用して、リストに追加されるプロパティ セット内のプロパティを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

