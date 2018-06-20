---
title: PidLidTimeZone の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5eb9842da78541bc8c73cd5b2c52abeb927f9031
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802261"
---
# <a name="pidlidtimezone-canonical-property"></a>PidLidTimeZone の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
定期的なミーティングのタイム ゾーンに関する情報を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |LID_TIME_ZONE  <br/> |
|プロパティを設定します。  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x0000000C  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

**DispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) プロパティが設定されていない場合ですが、 **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) プロパティが TRUE と**LID_IS_EXCEPTION** ([の場合にこのプロパティが読み取りのみPidLidIsException](pidlidisexception-canonical-property.md)) は、FALSE にします。 下位ワードは、タイム ゾーン情報を格納するテーブルにインデックスを指定します。 上の word では、最上位のビットだけが読み取られます。 そのビットが設定されている場合、参照されているタイム ゾーンは見られません夏時間 (DST) は、それ以外の場合、夏時間の日付が[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)で詳細に説明の後に。 
  
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

