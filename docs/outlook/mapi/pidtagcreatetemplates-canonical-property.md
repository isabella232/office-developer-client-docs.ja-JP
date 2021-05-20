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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438184"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>PidTagCreateTemplates 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダイアログ ボックス テンプレートエントリ識別子を含む埋め込みテーブル オブジェクトが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|識別子:  <br/> |0x3604  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

コンテナー内に作成できるテンプレート オブジェクトを確認するには、このプロパティの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出します。 結果のオブジェクトは、コンテナー内に作成できるすべてのテンプレートのエントリ識別子を与える 1 回きりテーブルです。 
  
テンプレート オブジェクトを作成するには、コンテナー オブジェクトの **CreateEntry** メソッド **を PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列の値を 1 回のテーブルから呼び出します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

