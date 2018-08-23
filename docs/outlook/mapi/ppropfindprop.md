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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f720160193613bbbb4bbd447f78c14e6e5378eb8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565656"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロパティで指定したプロパティの検索を設定します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>パラメーター

 _rgprop_
  
> [in]検索するプロパティを定義する[SPropValue](spropvalue.md)構造体の配列です。 
    
 _cprop_
  
> [in]_Rgprop_パラメーターで指定されたプロパティ セット内のプロパティの数。 
    
 _ulPropTag_
  
> [in]_Rgprop_パラメーターで指定されたプロパティ セット内で検索するプロパティのプロパティ タグです。 
    
## <a name="return-value"></a>戻り値

 **PpropFindProp**は、一致がない場合、入力プロパティのタグ、または NULL に一致するプロパティを定義する、 [SPropValue](spropvalue.md)構造体を返します。 
  
## <a name="remarks"></a>注釈

プロパティを指定したタグには、PT_UNSPECIFIED の種類のプロパティが示されている場合**PpropFindProp**関数は、タグにプロパティの識別子にのみ一致するものを検索します。 それ以外の場合、プロパティの型を含め、全体のプロパティ タグの一致を検出し、識別されるプロパティを返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI では、 **PpropFindProp**メソッドを使用して、リストに追加されているプロパティのプロパティの設定を検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

