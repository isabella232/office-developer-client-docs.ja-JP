---
title: PidTagCreateTemplates 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269938"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>PidTagCreateTemplates 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダイアログボックステンプレートエントリ識別子を含む埋め込み table オブジェクトが格納されています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|識別子:  <br/> |0x3604  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>解説

コンテナー内で作成できるテンプレートオブジェクトの詳細については、このプロパティの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出してください。 結果のオブジェクトは、コンテナー内に作成できるすべてのテンプレートのエントリ識別子を付与する1回限りのテーブルです。 
  
template オブジェクトを作成するには、1回限りのテーブルから**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列の値に対して、container オブジェクトの**createentry**メソッドを呼び出します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

