---
title: PidTagBodyCrc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350926"
---
# <a name="pidtagbodycrc-canonical-property"></a>PidTagBodyCrc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージテキストの巡回冗長検査 (CRC) 値を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_BODY_CRC  <br/> |
|識別子:  <br/> |0x0e1c  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>解説

メッセージストアは、PT_LONG 値を生成する任意の CRC アルゴリズムを使用できます。 このプロパティは、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティが初めて設定されたときとその後に変更されたときの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドの一部として計算する必要があります。
  
クライアントアプリケーションは**PR_BODY_CRC**を使用して、 **PR_BODY**のプロパティまたはそのバリエーションに含まれるメッセージテキスト文字列の比較を支援します。 このプロパティを使用すると、クライアントは、メッセージテキストが変更されたときにすばやく簡単に検出できます。 **PR_BODY_CRC**を使用して、メッセージストアから**PR_BODY**を取得し、ローカルバージョンと比較するのではなく、パフォーマンスを大幅に向上させることができます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

