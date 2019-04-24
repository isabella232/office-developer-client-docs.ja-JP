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
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315821"
---
# <a name="pidtagabproviderid-canonical-property"></a>PidTagAbProviderId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーの[MAPIUID](mapiuid.md)構造が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|識別子:  <br/> |0x3615  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>解説

**MAPIUID**構造体は、コンテナー階層にこの特定のコンテナーを提供するアドレス帳プロバイダーを識別します。 値は、各プロバイダーに対して一意です。 
  
アドレス帳プロバイダーは、複数の識別子を提供できます。 たとえば、2つの異なるコンテナーを提供するプロバイダーは、各コンテナーの**PR_AB_PROVIDER_ID**一意識別子で公開できます。 
  
 **PR_AB_PROVIDER_ID**は、メッセージストアの**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティに似ています。 クライアントアプリケーションは、 **PR_AB_PROVIDER_ID**を使用して、アドレス帳階層テーブル内の関連する行を見つけることができます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[PidTagStoreProvider 標準プロパティ](pidtagstoreprovider-canonical-property.md)


[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

