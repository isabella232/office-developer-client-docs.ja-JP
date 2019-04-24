---
title: PidTagContentIntegrityCheck 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 30ed8053c9c3d77f4831da37ddd2456ad0564a5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331893"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>PidTagContentIntegrityCheck 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの送信者がメッセージの内容を漏洩から権限のない受信者に保護できるようにする、ASN. 1 コンテンツの整合性チェック値を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|識別子:  <br/> |0x0c00  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージコンテンツの否認不可を提供します。 **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) と組み合わせて使用することにより、メッセージの内容がその宛先に変更されないようにします。
  
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

