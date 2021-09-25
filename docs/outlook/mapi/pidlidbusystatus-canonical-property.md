---
title: PidLidBusyStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b0e0b20023d3ce18d6ffbc5363d15cd6e2a619d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563995"
---
# <a name="pidlidbusystatus-canonical-property"></a>PidLidBusyStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
予定に対するユーザーの空き時間情報を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidBusyStatus  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x00008205  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |予定表  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、オブジェクトによって記述されるイベントに対するユーザーの可用性を指定し、以下に指定する値の 1 つである必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |予定なし。  <br/> |
|0x00000001  <br/> |ユーザーに予定されている予定のイベントがあります。  <br/> |
|0x00000002  <br/> |予定あり。  <br/> |
|0x00000003  <br/> |外出中。  <br/> |
   
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

