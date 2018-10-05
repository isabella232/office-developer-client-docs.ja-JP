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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400343"
---
# <a name="pidlidlogduration-canonical-property"></a>PidLidLogDuration 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ジャーナル メッセージの分単位で、期間を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidLogDuration  <br/> |
|プロパティを設定します。  <br/> |PSETID_Log  <br/> |
|長い ID (LID):  <br/> |0x00008707  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |ジャーナル  <br/> |
   
## <a name="remarks"></a>備考

(分)、 **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) と**dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) のプロパティの違いをする必要があるアクティビティの期間です。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> プロパティとは、仕訳帳の許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

