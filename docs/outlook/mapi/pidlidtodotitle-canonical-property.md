---
title: PidLidToDoTitle 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339943"
---
# <a name="pidlidtodotitle-canonical-property"></a>PidLidToDoTitle 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
統合されたタスク一覧でこのメッセージオブジェクトを識別するためのユーザー specifiable テキストを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidToDoTitle  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x000085a4  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、タスクに設定してはなりません。 空のプロパティを指定する場合は、このプロパティを長さ0の文字列に設定しないで、削除します。 
  
message オブジェクトのフラグを設定したときに、そのプロパティが存在しない場合、クライアントはこのプロパティに**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) の値を書き込む必要があります。
  
統合されたタスク一覧でこのプロパティが存在しない場合は、このプロパティをタスク一覧に表示するときに、クライアントは**PR_NORMALIZED_SUBJECT**プロパティの値を置換する必要があります。 
  
下書きのメッセージオブジェクトで、クライアントが sender フラグを実装している場合、このプロパティは**dispidrequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) と同じ値に設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidTagNormalizedSubject 標準プロパティ](pidtagnormalizedsubject-canonical-property.md)
  
[PidLidFlagRequest ���K���̃v���p�e�B](pidlidflagrequest-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

