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
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570437"
---
# <a name="fpropexists"></a>FPropExists

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**IMAPIProp**、 [IMessage](imessageimapiprop.md)や[IMAPIFolder](imapifolderimapicontainer.md)などから派生した[IMAPIProp](imapipropiunknown.md)インターフェイスまたはインターフェイスの指定されたプロパティ タグを検索します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>パラメーター

 _pobj_
  
> [in]**IMAPIProp**インターフェイス内のプロパティ タグを検索する**IMAPIProp**から派生したインターフェイスへのポインター。 
    
 _ulPropTag_
  
> [in]検索するプロパティ タグです。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> 指定されたプロパティ タグの一致が見つかりました。 
    
FALSE 
  
> 指定されたプロパティ タグの一致は見つかりませんでした。
    
## <a name="remarks"></a>注釈

型 PT_UNSPECIFIED、 _ulPropTag_パラメーターのプロパティ タグの場合、 **FPropExists**関数は、プロパティの識別子にのみ基づいて一致するを探します。 それ以外の場合、一致が、型を含め、全体のプロパティ タグです。 
  

