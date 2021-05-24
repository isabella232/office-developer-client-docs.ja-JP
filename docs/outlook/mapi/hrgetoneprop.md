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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 95273bf6025d6ef995d7c21c0e44bdbbf59072f6
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589174"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ インターフェイス 、つまり [IMAPIProp](imapipropiunknown.md)から派生したインターフェイスから 1 つのプロパティの値を取得します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
HRESULT HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>パラメーター

 _pmp_
  
> [in]プロパティ値 [を取得する IMAPIProp](imapipropiunknown.md) インターフェイスへのポインター。 
    
 _ulPropTag_
  
> [in]取得するプロパティのプロパティ タグ。 
    
 _ppprop_
  
> [out]取得したプロパティ値を定義する、返される [SPropValue](spropvalue.md) 構造体へのポインターを指すポインター。 
    
## <a name="return-value"></a>戻り値

MAPI_E_NOT_FOUND 
  
> 要求されたプロパティは、指定したインターフェイスから使用できません。
    
## <a name="remarks"></a>解説

[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドとは異なり **、HrGetOneProp** 関数は警告を返しません。 プロパティは 1 つしか取得しないので、単に成功または失敗します。 複数のプロパティを取得する場合 **、GetProps の方が** 高速です。 
  
[HrSetOneProp](hrsetoneprop.md)関数を使用して、1 つのプロパティを設定または変更できます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI は **、HrGetOneProp** メソッドを使用してオブジェクトの種類を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

