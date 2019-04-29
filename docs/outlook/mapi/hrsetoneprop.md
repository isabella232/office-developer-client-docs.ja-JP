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
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417659"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティインターフェイスの1つのプロパティの値を設定または変更します。つまり、 [imapiprop](imapipropiunknown.md)から派生したインターフェイスです。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>パラメーター

 _pmp_
  
> 順番プロパティ値を設定または変更する[imapiprop](imapipropiunknown.md)インターフェイスへのポインター。 
    
 _pprop_
  
> 順番_pmp_プロパティに設定する値を定義する[spropvalue](spropvalue.md)構造体へのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

[imapiprop:: setprops](imapiprop-setprops.md)メソッドとは異なり、 **hrsetoneprop**関数は警告を返しません。 1つのプロパティしか設定しないため、成功または失敗のどちらかです。 複数のプロパティを設定または変更する場合は、 **setprops**の方が高速です。 
  
[hrgetoneprop](hrgetoneprop.md)関数を使用して、1つのプロパティを取得できます。 
  

