---
title: PidLidReminderOverride 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderOverride
api_type:
- COM
ms.assetid: ad7e37e1-bd12-409f-87e5-ebc0c298a072
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4956ce33d00135c34193dec3df832c6878b2c6db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360109"
---
# <a name="pidlidreminderoverride-canonical-property"></a>PidLidReminderOverride 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントが **dispidReminderPlaySound** [(PidLidReminderPlaySound)](pidlidreminderplaysound-canonical-property.md)および **dispidReminderFileParam** ( [ PidLidReminderFileParameter](pidlidreminderfileparameter-canonical-property.md)) プロパティの値を尊重するかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidReminderOverride  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x0000851C  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは **、dispidReminderPlaySound** プロパティおよび **dispidReminderFileParam** プロパティの値に代わる既定値を使用できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> メールなどのオブジェクトアラームのプロパティと対話モデルを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

