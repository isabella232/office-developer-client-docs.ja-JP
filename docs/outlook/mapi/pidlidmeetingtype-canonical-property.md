---
title: PidLidMeetingType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 24b6d94dbd068698914d8bbd96a7b23f7cb2ae65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555735"
---
# <a name="pidlidmeetingtype-canonical-property"></a>PidLidMeetingType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
会議出席依頼または会議の更新の種類を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidMeetingType  <br/> |
|プロパティ セット:  <br/> |PSETID_Meeting  <br/> |
|長い ID (LID):  <br/> |0x00000026  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値は、次のいずれかの値に設定する必要があります。
  
|**プロパティ**|**値**|**説明**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |未指定。  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |最初の会議出席依頼。  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |完全な更新。  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |情報更新。  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |この後、新しい会議出席依頼または会議の更新プログラムが受信された。  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |これは、代理人が会議関連のオブジェクトを処理する場合に、委任者のコピーに設定されます。  <br/> |
   
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

