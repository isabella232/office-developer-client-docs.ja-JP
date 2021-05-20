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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429489"
---
# <a name="fpropexists"></a>FPropExists

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPIProp](imapipropiunknown.md)インターフェイスまたは [IMessage](imessageimapiprop.md)や **IMAPIFolder などの IMAPIProp** から派生したインターフェイスで、特定のプロパティ タグ [を検索します](imapifolderimapicontainer.md)。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>パラメーター

 _pobj_
  
> [in]プロパティ タグを **検索する IMAPIProp** から派生した **IMAPIProp** インターフェイスまたはインターフェイスへのポインター。 
    
 _ulPropTag_
  
> [in]検索するプロパティ タグ。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定されたプロパティ タグの一致が見つかりました。 
    
FALSE 
  
> 指定されたプロパティ タグの一致が見つかりませんでした。
    
## <a name="remarks"></a>注釈

_ulPropTag_ パラメーターのプロパティ タグに型 PT_UNSPECIFIED がある場合 **、FPropExists** 関数はプロパティ識別子にのみ基づいて一致を検索します。 それ以外の場合は、型を含むプロパティ タグ全体が一致します。 
  

