---
title: PidLidCalendarType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8e3017d18491fde6b66c3173c43b8b9d0ee37ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801834"
---
# <a name="pidlidcalendartype-canonical-property"></a>PidLidCalendarType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
**DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) のプロパティから [カレンダーの種類] フィールドの値を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |LID_CALENDAR_TYPE  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x0000001C  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

会議出席依頼は、一連の定期的なまたは例外を表している場合は、 **dispidApptRecur**プロパティから [カレンダーの種類] フィールドの値になります。 それ以外の場合、このプロパティは設定されず、0 と見なされます。 
  
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

