---
title: PidLidAllAttendeesString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 11b4ea96283bbef2dcb9afb109a6a81102727efc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570458"
---
# <a name="pidlidallattendeesstring-canonical-property"></a>PidLidAllAttendeesString 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
リソースと連絡先の参加者を含め、開催者以外のすべての出席者の一覧を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidAllAttendeesString  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008238  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

各出席者の値は、出席者の表示名です。 別のエントリは、スペースの後にセミコロンで区切る必要があります。 このプロパティが必要ではありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

