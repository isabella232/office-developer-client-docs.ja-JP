---
title: PidLidTaskResetReminder の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a95fc30de7511672cb27c9dd6fbc37b96e822e77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802240"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a>PidLidTaskResetReminder の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
**DispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) が FALSE である場合でも、定期的な仕事の将来のインスタンスに通知が必要なかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidTaskResetReminder  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008107  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

タスクのアラームを閉じる、およびそれ以外の場合は FALSE に設定すると、この値は TRUE に設定します。 未設定のままに、既定値は FALSE と見なされます。
  
[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)で指定したとは、 **dispidReminderSet**プロパティは、タスクにアラームを設定するかどうかを示します。 ただし、このプロパティには、1 つのタスクにアラームが存在することだけを示します。 アラームが定期的な仕事の将来のインスタンスに必要があるかどうかを確認するには、単独で使用できません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。
    
[[MS OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> 電子メールおよびその他のオブジェクトのアラームの操作モデルのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[PidLidReminderSet ���K���̃v���p�e�B](pidlidreminderset-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

