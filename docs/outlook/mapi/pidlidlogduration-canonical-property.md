---
title: PidLidLogDuration 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336919"
---
# <a name="pidlidlogduration-canonical-property"></a>PidLidLogDuration 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ジャーナルメッセージの期間 (分単位) を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidlogduration  <br/> |
|プロパティセット:  <br/> |PSETID_Log  <br/> |
|ロング ID (LID):  <br/> |0x00008707  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |仕訳帳  <br/> |
   
## <a name="remarks"></a>解説

**dispidlogend** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) プロパティと**dispidlogend** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) プロパティの間の差になる必要があるアクティビティの期間 (分単位)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> 仕訳帳に対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

