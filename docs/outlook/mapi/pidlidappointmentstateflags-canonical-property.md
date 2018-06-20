---
title: PidLidAppointmentStateFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801805"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a>PidLidAppointmentStateFlags の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
オブジェクトの状態を示すビット フィールドを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidApptStateFlags  <br/> |
|プロパティを設定します。  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008217  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>備考

このプロパティが必要ではありません。 以下は、個々 のフラグを設定することができます。
  
M (asfMeeting、0x00000001)
  
> このフラグは、オブジェクトが、会議オブジェクト、または会議に関連するオブジェクトであることを示します。
    
R (asfReceived、0x00000002)
  
> このフラグは、表示されたオブジェクトが他のユーザーから受信されたことを示します。
    
C (asfCanceled、0x00000004)
  
> このフラグは、オブジェクトによって表される、会議オブジェクトがキャンセルされたことを示します。
    
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

