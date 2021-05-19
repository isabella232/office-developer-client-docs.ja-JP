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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419255"
---
# <a name="pidtagdetailstable-canonical-property"></a>PidTagDetailsTable 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
埋め込み表示テーブル オブジェクトが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DETAILS_TABLE  <br/> |
|識別子:  <br/> |0x3605  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティを [オブジェクトの IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドに渡す場合、表示テーブルの作成を可能にする [IMAPITable](imapitableiunknown.md) インターフェイスが返されます。 MAPI では、このテーブルを使用して [、IAddrBook::D](iaddrbook-details.md) 呼び出しに応答してアドレス帳オブジェクトのプロパティ シートを表示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[PidTagSearch 標準プロパティ](pidtagsearch-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

