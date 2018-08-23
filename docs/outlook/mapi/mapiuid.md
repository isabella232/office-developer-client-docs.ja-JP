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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f7ec60768ab07c56969f538f196a1f9df5dbed17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587167"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
サービス プロバイダーを一意に識別するために使用する[GUID](guid.md)構造体のバイト順の独立したバージョンです。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Members

 **ab**
  
> 16 バイトの識別子を格納する配列。
    
## <a name="remarks"></a>注釈

**MAPIUID**構造体は、Intel® プロセッサのバイト順に格納する**GUID**構造体です。 
  
MAPI では、同じ識別子を持つ 2 つの異なる項目の非常にまれな方法で**MAPIUID**の構造体を作成します。 **MAPIUID**構造体は、バイナリ プロパティ、または、バイトの順序を保存するか、または情報にアクセスするコンピューターに関係なく、ファイルとして保存できます。 
  
 **MAPIUID**構造体が使用されます。 
  
- プロファイル セクションを確認します。
    
- エントリには、メッセージの識別子は、格納し、担当のサービス プロバイダーを識別するオブジェクトをブックに対応します。
    
- メッセージの**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティです。
    
検索キーの**MAPIUID**の識別子を生成するには、サービス プロバイダーは、 [IMAPISupport::NewUID](imapisupport-newuid.md)を呼び出します。
  
クライアントは、ネットワーク経由でメッセージを送信、ときに、プロトコルや送信の形式で、 **MAPIUID**のデータのバイト順を変更することはないを使用してください。 
  
**MAPIUID**構造体を使用する方法の詳細については、次のトピックを参照してください。 
  
[サービス プロバイダー一意識別子の登録](registering-service-provider-unique-identifiers.md)
  
[転送順序の設定](setting-transport-order.md)
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[MAPI の構造](mapi-structures.md)

