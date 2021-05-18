---
title: PidLidRecurrenceType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7a0ea0dfe236341815fe94fb570908d7034fc83e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315912"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>PidLidRecurrenceType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
定期的な系列の定期的な種類を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidRecurType  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008231  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、次に示す値のいずれかを使用して、定期的な系列の定期的な種類を指定します。
  
|**状態**|**値**|**説明**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |1 つのインスタンス予定。  <br/> |
|rectypeDaily  <br/> |1  <br/> |毎日の定期的なパターン。  <br/> |
|rectypeWeekly  <br/> |2  <br/> |毎週の定期的なパターン。  <br/> |
|rectypeMonthly  <br/> |3  <br/> |毎月の定期的なパターン。  <br/> |
|rectypeYearly  <br/> |4  <br/> |年次の定期的なパターン。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

