---
title: PidLidToDoTitle 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b93ff05c13ab9801e9830e36aeecdf942e53d233
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583640"
---
# <a name="pidlidtodotitle-canonical-property"></a>PidLidToDoTitle 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
統合された to-do リストでこのメッセージ オブジェクトを識別するためのユーザー指定可能なテキストが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidToDoTitle  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085A4  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、タスクで設定する必要があります。 空のプロパティを指定するには、このプロパティを長さ 0 の文字列に設定するのではなく、削除します。 
  
メッセージ オブジェクトにフラグを設定し、プロパティが存在しない場合、クライアントは **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) の値をこのプロパティに書き込む必要があります。
  
統合 To Do リストで、このプロパティが存在しない場合、クライアントは、このプロパティを to-do リストに表示 **するときに PR_NORMALIZED_SUBJECT** プロパティの値を置き換える必要があります。 
  
下書きメッセージ オブジェクトで、クライアントが送信者フラグを実装する場合、このプロパティは **dispidRequest** ([PidLidFlagRequest)](pidlidflagrequest-canonical-property.md)と同じ値に設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidTagNormalizedSubject 標準プロパティ](pidtagnormalizedsubject-canonical-property.md)
  
[PidLidFlagRequest ���K���̃v���p�e�B](pidlidflagrequest-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

