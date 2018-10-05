---
title: PidLidAppointmentColor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399873"
---
# <a name="pidlidappointmentcolor-canonical-property"></a>PidLidAppointmentColor 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
予定表を表示するときに使用する色を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptColor  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008214  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、予定表を表示するときに使用する色を指定します。 クライアントまたはサーバーは、古いクライアントとの下位互換性のためには、この値を設定する必要があります。 カレンダーで指定した[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)として**のキーワード**([PidNameKeywords](pidnamekeywords-canonical-property.md)) プロパティの値に基づくことが代わりに表示されます。 設定すると、値があります、次のいずれかです。
  
|**値**|**色**|
|:-----|:-----|
|0x00000000  <br/> |なし  <br/> |
|0x00000001  <br/> |赤  <br/> |
|0x00000002  <br/> |青  <br/> |
|0x00000003  <br/> |緑  <br/> |
|0x00000004  <br/> |灰色  <br/> |
|0x00000005  <br/> |オレンジ  <br/> |
|0x00000006  <br/> |シアン  <br/> |
|0x00000007  <br/> |オリーブ  <br/> |
|0x00000008  <br/> |紫  <br/> |
|0x00000009  <br/> |青緑  <br/> |
|0x0000000A  <br/> |黄  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

