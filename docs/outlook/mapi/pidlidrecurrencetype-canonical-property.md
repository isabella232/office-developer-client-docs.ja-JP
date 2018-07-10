---
title: PidLidRecurrenceType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9fecd67c370333064fd593634ad2a924a3005d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802102"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>PidLidRecurrenceType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
定期的な一連の定期的なアイテムの種類を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidRecurType  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008231  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |カレンダー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、次の値のいずれかを使用して定期的な一連の定期的なアイテムの種類を指定します。
  
|**Status**|**値**|**説明**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |単一インスタンスの予定です。  <br/> |
|rectypeDaily  <br/> |1  <br/> |毎日の定期的なパターンです。  <br/> |
|rectypeWeekly  <br/> |2  <br/> |毎週定期的なパターンを使用します。  <br/> |
|rectypeMonthly  <br/> |3  <br/> |毎月の定期的なパターンです。  <br/> |
|rectypeYearly  <br/> |4  <br/> |年間の定期的なパターンです。  <br/> |
   
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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
