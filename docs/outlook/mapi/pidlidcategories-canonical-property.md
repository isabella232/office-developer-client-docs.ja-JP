---
title: PidLidCategories 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344976"
---
# <a name="pidlidcategories-canonical-property"></a>PidLidCategories 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムのカテゴリの一覧を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidCategories  <br/> |
|プロパティ セット:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|長い ID (LID):  <br/> |0x00002328  <br/> |
|データの種類 :   <br/> |PT_MV_UNICODE  <br/> |
|エリア:  <br/> |共通  <br/> |
   
## <a name="remarks"></a>注釈

キーワード ヘッダー フィールドを生成するには、クライアントは、このプロパティの値を目的の値に設定する必要があります。 このプロパティには複数の文字列があります。各カテゴリは 1 つのキーワードにマップする必要があります。
  
多目的インターネット メール拡張機能 (MIME) ライターは、このプロパティの各サブ値を[キーワード] ヘッダー フィールドの個別のキーワードにコピーし、各キーワードをコンマ (U+002C) とスペース (U+0020) で区切る必要があります。 MIME ライターは、異なる組織の異なるカテゴリ セット間の競合を回避するために、このプロパティをキーワード ヘッダー フィールドにコピーする代わりに、このプロパティを削除できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

