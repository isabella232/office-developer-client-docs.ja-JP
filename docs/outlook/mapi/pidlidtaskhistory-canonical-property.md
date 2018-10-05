---
title: PidLidTaskHistory 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391942"
---
# <a name="pidlidtaskhistory-canonical-property"></a>PidLidTaskHistory 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクを最後に加えられた変更の種類を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskHistory  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x0000811A  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値を設定すると、 **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) のプロパティは現在の時刻にも設定しなければなりません。 次の表は、 **dispidTaskHistory**プロパティの値を優先度順に一覧表示を示しています。 
  
|**値**|**説明**|
|:-----|:-----|
|0x00000004  <br/> |**DispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) のプロパティを変更します。  <br/> |
|0x00000003  <br/> |別のプロパティが変更されました。  <br/> |
|0x00000001  <br/> |タスク実施者は、このタスクを承諾します。  <br/> |
|0x00000002  <br/> |タスク実施者は、このタスクを拒否します。  <br/> |
|0x00000005  <br/> |タスクは、タスクの実施者に割り当てられました。  <br/> |
|0x00000000  <br/> |変更は行われませんでした。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

