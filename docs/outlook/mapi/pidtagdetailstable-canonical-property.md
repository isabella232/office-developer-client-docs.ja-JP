---
title: PidTagDetailsTable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1602d1753d9f7f6e6f407a85dab0a33255db7aae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585788"
---
# <a name="pidtagdetailstable-canonical-property"></a>PidTagDetailsTable 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
埋め込み表示テーブル オブジェクトが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DETAILS_TABLE  <br/> |
|識別子:  <br/> |0x3605  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティをオブジェクトの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドに渡すことは、表示された表の作成を可能にする[IMAPITable](imapitableiunknown.md)インターフェイスを返します。 MAPI では、このテーブルを使用して、 [IAddrBook::Details](iaddrbook-details.md)の呼び出しへの応答で、アドレス帳のオブジェクトのプロパティ シートを表示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagCreateTemplates 標準プロパティ Property](pidtagcreatetemplates-canonical-property.md)
  
[PidTagSearch 標準プロパティ](pidtagsearch-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

