---
title: PidLidAppointmentAuxiliaryFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 66bbaccb056dfeba28d3016023a8093bc05927b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591970"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a>PidLidAppointmentAuxiliaryFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの補助状態を表すビット フィールドを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidApptAuxFlags  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008207  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは必須ではありません。 以下に、設定できる個別のフラグを示します。
  
C (auxApptFlagCopied、0x00000001)
  
> このフラグは、calendar オブジェクトが別の予定表フォルダーからコピーされたかどうかを示します。
    
R (auxApptFlagForceMtgResponse,0x00000002)
  
> 会議出席依頼のこのフラグは、クライアントまたはサーバーが、応答が選択された場合に会議の応答を開催者に返す必要があります。
    
F (auxApptFlagForwarded、0x00000004)
  
> 会議出席依頼のこのフラグは、開催者からの招待ではなく、転送 (開催者による転送を含む) を示します。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
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

