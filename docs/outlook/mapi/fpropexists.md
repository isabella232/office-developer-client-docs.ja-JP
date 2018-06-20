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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800123"
---
# <a name="fpropexists"></a>FPropExists

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _pobj_
  
> [in]**IMAPIProp**インターフェイス内のプロパティ タグを検索する**IMAPIProp**から派生したインターフェイスへのポインター。 
    
 _ulPropTag_
  
> [in]検索するプロパティ タグです。
    
## <a name="return-value"></a>�߂�l

TRUE 
  
> 指定されたプロパティ タグの一致が見つかりました。 
    
FALSE 
  
> 指定されたプロパティ タグの一致は見つかりませんでした。
    
## <a name="remarks"></a>備考

型 PT_UNSPECIFIED、 _ulPropTag_パラメーターのプロパティ タグの場合、 **FPropExists**関数は、プロパティの識別子にのみ基づいて一致するを探します。 それ以外の場合、一致が、型を含め、全体のプロパティ タグです。 
  

