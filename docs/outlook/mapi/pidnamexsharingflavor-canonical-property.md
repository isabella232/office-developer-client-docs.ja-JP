---
title: PidNameXSharingFlavor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e96fc2f39e8045847aa039b06f1f0ffaeb4a4917
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579216"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>PidNameXSharingFlavor 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**dispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) プロパティの値を表します。
  
|||
|:-----|:-----|
|分名:  <br/> |なし  <br/> |
|プロパティ セット:  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |X-Sharing-Flavor  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>注釈

**dispidSharingFlavor** プロパティは、次のいずれかの値である必要があります。 
  
|**値**|**共有メッセージの種類**|
|:-----|:-----|
|0x00020310  <br/> |特別なフォルダーの共有の招待。  <br/> |
|0x00000310  <br/> |特別なフォルダーではないフォルダーの共有の招待。  <br/> |
|0x00020500  <br/> |共有要求。  <br/> |
|0x00020710  <br/> |特別なフォルダーの共有の招待と、受信者と同等の特別なフォルダーの共有要求の両方。  <br/> |
|0x00025100  <br/> |要求を拒否する共有応答。  <br/> |
|0x00023310  <br/> |要求 (共有招待の種類) を受け入れる共有応答。  <br/> |
   
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

