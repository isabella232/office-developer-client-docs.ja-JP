---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dada6f5c1e9ddce388901d359766fe9a80c08f45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551577"
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
  

