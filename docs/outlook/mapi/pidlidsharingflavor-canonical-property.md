---
title: PidLidSharingFlavor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: df5cb7fe6a45b87d7a382c6d6a928711c0f90f62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600527"
---
# <a name="pidlidsharingflavor-canonical-property"></a>PidLidSharingFlavor 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
共有メッセージのプロパティとして指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidSharingFlavor  <br/> |
|プロパティ セット:  <br/> |PSETID_Sharing  <br/> |
|長い ID (LID):  <br/> |0x00008A18  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値は、次のいずれかを指定する必要があります。
  
|**値**|**共有メッセージ オブジェクトの種類**|
|:-----|:-----|
|0x00020310  <br/> |特別なフォルダーの共有の招待。  <br/> |
|0x00000310  <br/> |特別なフォルダーではないフォルダーの共有の招待。  <br/> |
|0x00020500  <br/> |共有要求。  <br/> |
|0x00020710  <br/> |特別なフォルダーの共有の招待と、受信者と同等の特別なフォルダーの共有要求の両方。  <br/> |
|0x00025100  <br/> |要求を拒否する共有応答。  <br/> |
|0x00023310  <br/> |要求を受け入れる共有応答 (共有招待の種類も含む)。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> クライアント間でメールボックス フォルダーを共有します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

