---
title: PidTagAbProviderId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 30569efe44960486940e0b39b44ca43d911a8b76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561041"
---
# <a name="pidtagabproviderid-canonical-property"></a>PidTagAbProviderId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーの [MAPIUID 構造を含](mapiuid.md) む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|識別子:  <br/> |0x3615  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

**MAPIUID 構造体は**、コンテナー階層でこの特定のコンテナーを提供するアドレス帳プロバイダーを識別します。 値は、各プロバイダーに固有です。 
  
アドレス帳プロバイダーは、複数の識別子を指定できます。 たとえば、2 つの異なるコンテナーを提供するプロバイダーは、各コンテナー PR_AB_PROVIDER_ID一 **意** の識別子を発行できます。 
  
 **PR_AB_PROVIDER_ID** は、メッセージ ストアの PR_MDB_PROVIDER **(** [PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティに類似しています。 クライアント アプリケーションは **、PR_AB_PROVIDER_IDを** 使用して、アドレス帳階層テーブル内の関連する行を検索できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[PidTagStoreProvider 標準プロパティ](pidtagstoreprovider-canonical-property.md)


[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

