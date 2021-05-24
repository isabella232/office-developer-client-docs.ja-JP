---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9fae06b9e9d5ef4885d798825659fa3486ec9e72
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589181"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ インターフェイス [(IMAPIProp](imapipropiunknown.md)から派生したインターフェイス) の 1 つのプロパティの値を設定または変更します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
HRESULT HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>パラメーター

 _pmp_
  
> [in]プロパティ値 [を設定または変更する IMAPIProp](imapipropiunknown.md) インターフェイスへのポインター。 
    
 _pprop_
  
> [in]_pmp_ プロパティに設定する値を定義する [SPropValue](spropvalue.md)構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドとは異なり **、HrSetOneProp** 関数は警告を返しません。 プロパティは 1 つしか設定しないので、単に成功または失敗します。 複数のプロパティを設定または変更する場合 **、SetProps の方が** 高速です。 
  
HrGetOneProp 関数を使用して [1 つのプロパティを取得](hrgetoneprop.md) できます。 
  

