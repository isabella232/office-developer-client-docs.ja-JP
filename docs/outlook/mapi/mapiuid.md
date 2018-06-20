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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3675c6a8ee2ee208f175dd5f7d219447aa52e9ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801540"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

 **ab**
  
> 16 バイトの識別子を格納する配列。
    
## <a name="remarks"></a>備考

**MAPIUID**構造体は、Intel® プロセッサのバイト順に格納する**GUID**構造体です。 
  
MAPI では、同じ識別子を持つ 2 つの異なる項目の非常にまれな方法で**MAPIUID**の構造体を作成します。 **MAPIUID**構造体は、バイナリ プロパティ、または、バイトの順序を保存するか、または情報にアクセスするコンピューターに関係なく、ファイルとして保存できます。 
  
 **MAPIUID**構造体が使用されます。 
  
- プロファイル セクションを確認します。
    
- エントリには、メッセージの識別子は、格納し、担当のサービス プロバイダーを識別するオブジェクトをブックに対応します。
    
- メッセージの**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティです。
    
検索キーの**MAPIUID**の識別子を生成するには、サービス プロバイダーは、 [IMAPISupport::NewUID](imapisupport-newuid.md)を呼び出します。
  
クライアントは、ネットワーク経由でメッセージを送信、ときに、プロトコルや送信の形式で、 **MAPIUID**のデータのバイト順を変更することはないを使用してください。 
  
**MAPIUID**構造体を使用する方法の詳細については、次のトピックを参照してください。 
  
[サービス プロバイダーの一意の識別子を登録します。](registering-service-provider-unique-identifiers.md)
  
[トランスポート オーダを設定](setting-transport-order.md)
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[MAPI の構造](mapi-structures.md)

