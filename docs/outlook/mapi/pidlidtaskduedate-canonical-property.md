---
title: PidLidTaskDueDate の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d26a686573a9dc178a46b7dfdc5c18485303b7ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802217"
---
# <a name="pidlidtaskduedate-canonical-property"></a>PidLidTaskDueDate の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ユーザーがタスクの完了に必要とする日付を表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidTaskDueDate  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008105  <br/> |
|データを入力します。  <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

このプロパティが未設定またはに設定の 0x5AE980E0 (1,525,252,320) である場合、タスクの締め切り日はありません。 ただし、 **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) のプロパティの開始日が指定されていない場合にだけは、期日はオプションです。 タスクに期限がある場合は、値が午前 0 時という時刻成分を持つ必要があり、 **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) のプロパティを設定する必要がありますもします。 **DispidTaskStartDate**に開始日が設定されている場合、 **dispidTaskDueDate**プロパティの値を必要があります**dispidTaskStartDate**の値以上です。
  
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



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
