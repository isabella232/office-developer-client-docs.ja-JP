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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 31d2be027ef3b58fdd44e71c922677164d352feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569128"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
インターフェイスでは、プロパティ、つまり、 [IMAPIProp](imapipropiunknown.md)から派生したインターフェイスの 1 つのプロパティの値を変更または設定します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>パラメーター

 _pmp_
  
> [in]プロパティの値を設定または変更するのになっている[IMAPIProp](imapipropiunknown.md)インターフェイスへのポインター。 
    
 _pprop_
  
> [in]_Pmp_プロパティに設定する値を定義する[SPropValue](spropvalue.md)構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドとは異なり、 **HrSetOneProp**関数は決して警告を返します。 1 つのプロパティを設定しているため、単に成功または失敗します。 設定、または複数のプロパティを変更する、 **SetProps**が高速です。 
  
[HrGetOneProp](hrgetoneprop.md)関数を使用して 1 つのプロパティを取得することができます。 
  

