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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386867"
---
# <a name="pidlidtaskstatus-canonical-property"></a>PidLidTaskStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクのユーザーの進行状況のステータスを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskStatus  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008101  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値を次のいずれかに設定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |ユーザーは、タスクの作業を開始されていません。 この値が設定されている場合、 **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) は、0.0 をする必要があります。  <br/> |
|0x00000001  <br/> |このタスクでのユーザーの作業は進行中です。 この値が設定されている場合、 **dispidPercentComplete**は 0.0 および 1.0 未満の場合よりも大きくなければなりません。  <br/> |
|0x00000002  <br/> |このタスクでのユーザーの作業は完了です。 この値が設定されている場合は、 **dispidPercentComplete**は 1.0 である必要があり、 **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) は、現在の日付である必要があります**dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) は TRUE である必要があります。  <br/> |
|0x00000003  <br/> |ユーザーは、他のユーザーに待機しています。  <br/> |
|0x00000004  <br/> |ユーザーは、タスクの作業を延期しました。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。
    
[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
[[MS OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。
    
[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidPercentComplete 標準プロパティ](pidlidpercentcomplete-canonical-property.md)
  
[PidLidTaskDateCompleted 標準プロパティ](pidlidtaskdatecompleted-canonical-property.md)
  
[PidLidTaskComplete 標準プロパティ](pidlidtaskcomplete-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

