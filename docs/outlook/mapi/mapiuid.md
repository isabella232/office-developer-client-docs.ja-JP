---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 807d517c2856c52ca47838f0927db44b0b7dda68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579467"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーを一意に識別するために使用される [GUID](guid.md) 構造のバイトオーダー独立バージョン。 
  
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
  
> 16 バイトの識別子を含む配列。
    
## <a name="remarks"></a>注釈

**MAPIUID 構造は****、Intel** のプロセッサ バイトオーダーに® GUID 構造です。 
  
MAPI は **、2 つの** 異なるアイテムが同じ識別子を持つ非常にまれな方法で MAPIUID 構造体を作成します。 **MAPIUID** 構造体は、情報を格納またはアクセスするコンピューターのバイト順序に関係なく、バイナリ プロパティまたはファイルとして格納できます。 
  
 **MAPIUID** 構造が使用されます。 
  
- プロファイル セクションを識別します。
    
- メッセージ ストアオブジェクトとアドレス帳オブジェクトのエントリ識別子で、責任あるサービス プロバイダーを識別します。
    
- メッセージの **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティ。
    
検索キーの **MAPIUID 識別子** を生成するために、サービス プロバイダーは [IMAPISupport::NewUID を呼び出します](imapisupport-newuid.md)。
  
クライアントがネットワークを通してメッセージを送信する場合、MAPIUID データのバイトオーダーを変更しないプロトコルまたは送信形式 **を使用する必要** があります。 
  
**MAPIUID 構造体の使用方法の** 詳細については、次のトピックを参照してください。 
  
[サービス プロバイダーの一意の識別子の登録](registering-service-provider-unique-identifiers.md)
  
[トランスポートの順序の設定](setting-transport-order.md)
  
## <a name="see-also"></a>関連項目



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[MAPI の構造](mapi-structures.md)

