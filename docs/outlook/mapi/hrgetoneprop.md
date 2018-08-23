---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 99b63e7b0b31a603bf372b1d52e83af39784b628
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564158"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロパティのインターフェイスから、つまり、 [IMAPIProp](imapipropiunknown.md)から派生したインターフェイスには、1 つのプロパティの値を取得します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>パラメーター

 _pmp_
  
> [in][IMAPIProp](imapipropiunknown.md)インターフェイスを取得するプロパティの値は、元へのポインター。 
    
 _ulPropTag_
  
> [in]取得するプロパティのプロパティ タグです。 
    
 _ppprop_
  
> [out]取得したプロパティ値を定義する、返される[SPropValue](spropvalue.md)構造へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

MAPI_E_NOT_FOUND 
  
> 要求されたプロパティは、指定されたインターフェイスからは使用できません。
    
## <a name="remarks"></a>注釈

、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドとは異なり、 **HrGetOneProp**関数は決して警告を返します。 1 つのプロパティを取得するために単に成功または失敗します。 複数のプロパティを取得するため**GetProps**が高速です。 
  
設定または[HrSetOneProp](hrsetoneprop.md)関数を使用して 1 つのプロパティを変更できます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI では、 **HrGetOneProp**メソッドを使用して、オブジェクトの種類を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

