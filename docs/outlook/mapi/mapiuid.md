---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432206"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダーを一意に識別するために使用される[GUID](guid.md)構造のバイト順序に依存しないバージョン。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>メンバー

 **l**
  
> 16バイトの識別子を含む配列。
    
## <a name="remarks"></a>注釈

**MAPIUID**構造体は、Intel ®プロセッサのバイト順に格納される**GUID**構造です。 
  
MAPI は、2つの異なるアイテムが同じ識別子を持つようにする方法で、 **MAPIUID**構造を作成します。 **MAPIUID**構造体は、バイナリプロパティとして、または情報に格納またはアクセスするコンピューターのバイト順序に関係なく、ファイルとして保存できます。 
  
 **MAPIUID**構造体を使用します。 
  
- プロファイルセクションを識別する。
    
- メッセージストアとアドレス帳オブジェクトのエントリ識別子で、責任のあるサービスプロバイダを識別します。
    
- メッセージの**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティ。
    
検索キーの**MAPIUID**識別子を生成するために、サービスプロバイダーは[imapisupport:: newuid](imapisupport-newuid.md)を呼び出します。
  
クライアントがネットワーク経由でメッセージを送信する場合、 **MAPIUID**データのバイト順を変更しないプロトコルまたは転送形式を使用する必要があります。 
  
**MAPIUID**構造体の使用方法の詳細については、以下のトピックを参照してください。 
  
[サービスプロバイダーの一意識別子の登録](registering-service-provider-unique-identifiers.md)
  
[トランスポート順序の設定](setting-transport-order.md)
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[MAPI の構造](mapi-structures.md)

