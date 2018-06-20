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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803696"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _rgprop_
  
> [in]検索するプロパティを定義する[SPropValue](spropvalue.md)構造体の配列です。 
    
 _cprop_
  
> [in]_Rgprop_パラメーターで指定されたプロパティ セット内のプロパティの数。 
    
 _ulPropTag_
  
> [in]_Rgprop_パラメーターで指定されたプロパティ セット内で検索するプロパティのプロパティ タグです。 
    
## <a name="return-value"></a>�߂�l

 **PpropFindProp**は、一致がない場合、入力プロパティのタグ、または NULL に一致するプロパティを定義する、 [SPropValue](spropvalue.md)構造体を返します。 
  
## <a name="remarks"></a>備考

プロパティを指定したタグには、PT_UNSPECIFIED の種類のプロパティが示されている場合**PpropFindProp**関数は、タグにプロパティの識別子にのみ一致するものを検索します。 それ以外の場合、プロパティの型を含め、全体のプロパティ タグの一致を検出し、識別されるプロパティを返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI では、 **PpropFindProp**メソッドを使用して、リストに追加されているプロパティのプロパティの設定を検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

