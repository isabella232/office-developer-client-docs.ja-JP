---
title: PidLidAppointmentUnsendableRecipients 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidAppointmentUnsendableRecipients
api_type:
- COM
ms.assetid: ba154612-1b0f-4ef3-8d9f-7981b1c61a2c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dc273e757f173515e8c49827c1a55aa04e1faaf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801843"
---
# <a name="pidlidappointmentunsendablerecipients-canonical-property"></a>PidLidAppointmentUnsendableRecipients 標準プロパティ

  
  
**適用対象**: Outlook 
  
連絡先の出席者の一覧が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptUnsendableRecips  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000823D  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは必須ではありませんが、設定する必要があります。 形式は、 [[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で詳しく説明します。
  
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

