---
title: PidNameXSharingFlavor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameXSharingFlavor
api_type:
- COM
ms.assetid: 7757fde1-564b-4f3a-9b9e-f80a143690ea
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2afa598bf9b7949f2e9142611570ebbd048f7e3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392124"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>PidNameXSharingFlavor 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**DispidSharingFlavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) プロパティの値を表します。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |なし  <br/> |
|プロパティを設定します。  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |X 共有フレーバー  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>備考

**DispidSharingFlavor**プロパティは、次の値のいずれかである必要があります。 
  
|**値**|**共有メッセージの種類**|
|:-----|:-----|
|0x00020310  <br/> |特殊フォルダーの共有への招待。  <br/> |
|0x00000310  <br/> |特別なフォルダーではないフォルダーの共有への招待。  <br/> |
|0x00020500  <br/> |共有の依頼です。  <br/> |
|0x00020710  <br/> |両方共有への招待の特別なフォルダーと受信者の対応する特別なフォルダーの共有の依頼です。  <br/> |
|0x00025100  <br/> |共有の応答、要求を拒否します。  <br/> |
|0x00023310  <br/> |共有の応答 (も一種の共有への招待) の要求を受け入れる。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> クライアント間でのメールボックスのフォルダーを共有します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

