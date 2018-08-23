---
title: PidTagAbProviderId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802401"
---
# <a name="pidtagabproviderid-canonical-property"></a>PidTagAbProviderId 標準プロパティ

  
  
**適用対象**: Outlook 
  
アドレス帳プロバイダーの[MAPIUID](mapiuid.md)構造体が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|識別子:  <br/> |0x3615  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

**MAPIUID**構造体は、このコンテナーの階層内の特定のコンテナーを提供するアドレス帳プロバイダーを識別します。 値は、各プロバイダーに固有です。 
  
アドレス帳プロバイダーは、複数の識別子を提供できます。 などの異なる 2 つのコンテナーを提供するプロバイダーは、各コンテナーの一意の識別子を**PR_AB_PROVIDER_ID**で発行できます。 
  
 **PR_AB_PROVIDER_ID**は、メッセージ ・ ストアの**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) のプロパティに似ています。 クライアント アプリケーションは、アドレス帳の階層テーブルに関連する行を検索するのには**PR_AB_PROVIDER_ID**を使用することができます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[PidTagStoreProvider 標準プロパティ](pidtagstoreprovider-canonical-property.md)


[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

