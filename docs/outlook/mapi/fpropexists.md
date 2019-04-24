---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327273"
---
# <a name="fpropexists"></a>FPropExists

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[imapiprop](imapipropiunknown.md)インターフェイス内の指定されたプロパティタグ、または**imapiprop**( [IMessage](imessageimapiprop.md)や[imapiprop](imapifolderimapicontainer.md)など) から派生したインターフェイスを検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>パラメーター

 _pobj_
  
> 順番プロパティタグを検索する**imapiprop**から派生した**imapiprop**インターフェイスまたはインターフェイスへのポインター。 
    
 _ulPropTag_
  
> 順番検索するプロパティタグを指定します。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定したプロパティタグに一致するものが見つかりました。 
    
FALSE 
  
> 指定されたプロパティタグに一致するものが見つかりませんでした。
    
## <a name="remarks"></a>解説

_ulPropTag_パラメーターの property タグに type PT_UNSPECIFIED が指定されている場合、 **fpropexists**関数は、プロパティ識別子のみに基づいて一致を検索します。 それ以外の場合は、型を含むプロパティタグ全体の一致が照合されます。 
  

