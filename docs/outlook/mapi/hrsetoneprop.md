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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8af0d5c6eaff0c1e01e01c24c46f299e0c637f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800320"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _pmp_
  
> [in]プロパティの値を設定または変更するのになっている[IMAPIProp](imapipropiunknown.md)インターフェイスへのポインター。 
    
 _pprop_
  
> [in]_Pmp_プロパティに設定する値を定義する[SPropValue](spropvalue.md)構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドとは異なり、 **HrSetOneProp**関数は決して警告を返します。 1 つのプロパティを設定しているため、単に成功または失敗します。 設定、または複数のプロパティを変更する、 **SetProps**が高速です。 
  
[HrGetOneProp](hrgetoneprop.md)関数を使用して 1 つのプロパティを取得することができます。 
  

