---
title: PidTagStoreProvider 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c16f2477d107220408771328f4ad339774a696cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599376"
---
# <a name="pidtagstoreprovider-canonical-property"></a>PidTagStoreProvider 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアの種類を示すプロバイダー定義 [の MAPIUID](mapiuid.md) 構造体を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MDB_PROVIDER  <br/> |
|識別子:  <br/> |0x3414  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

[MAPIUID 構造体は](mapiuid.md)、メッセージ ストアの種類を識別します。 この値は、メッセージ ストア オブジェクト上のメッセージ ストア プロバイダーによって計算され、各プロバイダーに固有です。 通常、メッセージ ストア テーブルを参照して、パブリック フォルダーなどの目的の種類のストアを検索するために使用されます。 
  
このプロパティは、アドレス帳の PR_AB_PROVIDER_ID **(** [PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) プロパティに類似しています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

