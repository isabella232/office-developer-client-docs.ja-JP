---
title: PidLidTaskStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316668"
---
# <a name="pidlidtaskstatus-canonical-property"></a>PidLidTaskStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクのユーザーの進捗状況を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidtaskstatus  <br/> |
|プロパティセット:  <br/> |PSETID_Task  <br/> |
|ロング ID (LID):  <br/> |0x00008101  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値には、次のいずれかを設定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |ユーザーがタスクの作業を開始していません。 この値が設定されている場合、 **dispidpercentcomplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) は0.0 である必要があります。  <br/> |
|0x00000001  <br/> |このタスクでのユーザーの作業は進行中です。 この値が設定されている場合、 **dispidpercentcomplete**率は0.0 より大きく1.0 未満でなければなりません。  <br/> |
|0x00000002  <br/> |このタスクでのユーザーの作業は完了です。 この値が設定されている場合、 **dispidpercentcomplete**率は1.0 でなければなりません。 **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) は現在の日付で、 **dispidtaskcomplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) は TRUE である必要があります。  <br/> |
|0x00000003  <br/> |ユーザーが他のユーザーを待機しています。  <br/> |
|0x00000004  <br/> |ユーザーがタスクの作業を延期しました。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子メールをモデル化する複数のオブジェクトを定義します。
    
[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序と流れを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidPercentComplete 標準プロパティ](pidlidpercentcomplete-canonical-property.md)
  
[PidLidTaskDateCompleted 標準プロパティ](pidlidtaskdatecompleted-canonical-property.md)
  
[PidLidTaskComplete 標準プロパティ](pidlidtaskcomplete-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

