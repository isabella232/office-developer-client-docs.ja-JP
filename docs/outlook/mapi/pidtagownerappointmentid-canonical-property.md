---
title: PidTagOwnerAppointmentId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ad68a8ba527879871e79dd85e79d577291d32a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386049"
---
# <a name="pidtagownerappointmentid-canonical-property"></a>PidTagOwnerAppointmentId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
所有者のスケジュールで予定の識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_OWNER_APPT_ID  <br/> |
|識別子:  <br/> |0x0062  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Appointment  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、会議出席依頼で使用されます。 エントリの識別子ですが、送信者のスケジュールで予定を一意に識別する長整数型を表していません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。
    
[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
[[MS OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagOriginalAuthorSearchKey 標準プロパティ](pidtagoriginalauthorsearchkey-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

