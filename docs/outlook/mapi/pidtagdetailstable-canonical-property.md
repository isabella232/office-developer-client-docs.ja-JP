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
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360838"
---
# <a name="pidtagdetailstable-canonical-property"></a>PidTagDetailsTable 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
埋め込みの表示テーブルオブジェクトを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DETAILS_TABLE  <br/> |
|識別子:  <br/> |0x3605  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>解説

このプロパティを、オブジェクトの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドに渡すと、表示テーブルを作成できる[IMAPITable](imapitableiunknown.md)インターフェイスが返されます。 MAPI では、このテーブルを使用して、 [IAddrBook::D etails](iaddrbook-details.md)呼び出しへの応答として、アドレス帳オブジェクトのプロパティシートを表示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[PidTagSearch 標準プロパティ](pidtagsearch-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

