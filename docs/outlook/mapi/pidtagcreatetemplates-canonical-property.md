---
title: PidTagCreateTemplates 標準プロパティ Property
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
ms.openlocfilehash: 28611e442f816e4d091cc6b29e2ee69195a63d09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563360"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>PidTagCreateTemplates 標準プロパティ Property

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ダイアログ ボックス テンプレートのエントリの識別子を格納している埋め込みテーブル オブジェクトが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|識別子:  <br/> |0x3604  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

コンテナーの内部オブジェクトを作成するテンプレートについては、このプロパティの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 結果のオブジェクトは、コンテナー内に作成できるテンプレートをすべてのエントリの識別子を提供する一時テーブルです。 
  
テンプレート オブジェクトを作成するには、一時テーブルから**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) の列の値に、コンテナー オブジェクトの**CreateEntry**メソッドを呼び出します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

