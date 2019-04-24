---
title: PidTagStoreProvider 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278709"
---
# <a name="pidtagstoreprovider-canonical-property"></a>PidTagStoreProvider 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアの種類を示すプロバイダー定義の[MAPIUID](mapiuid.md)構造が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MDB_PROVIDER  <br/> |
|識別子:  <br/> |0x3414  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>解説

[MAPIUID](mapiuid.md)構造体は、メッセージストアの種類を識別します。 この値は、メッセージストアオブジェクトのメッセージストアプロバイダーによって計算され、各プロバイダーに対して一意です。 通常、メッセージストアテーブルを参照して、必要な種類 (パブリックフォルダーなど) のストアを検索するために使用されます。 
  
このプロパティは、アドレス帳の**PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) プロパティに似ています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

