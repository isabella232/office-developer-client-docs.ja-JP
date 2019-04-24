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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360887"
---
# <a name="pidnamexsharingflavor-canonical-property"></a>PidNameXSharingFlavor 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**dispidsharingflavor** ([PidLidSharingFlavor](pidlidsharingflavor-canonical-property.md)) プロパティの値を表します。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |なし  <br/> |
|プロパティセット:  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |X 共有-フレーバー  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>解説

**dispidsharingflavor**プロパティには、次のいずれかの値を指定する必要があります。 
  
|**値**|**共有メッセージの種類**|
|:-----|:-----|
|0x00020310  <br/> |特別なフォルダーの共有への招待。  <br/> |
|0x00000310  <br/> |特別なフォルダーではないフォルダーの共有への招待。  <br/> |
|0x00020500  <br/> |共有の依頼。  <br/> |
|0x00020710  <br/> |特別なフォルダーの共有への招待と、受信者の同等の特殊フォルダーに対する共有要求の両方。  <br/> |
|0x00025100  <br/> |要求を拒否する共有応答。  <br/> |
|0x00023310  <br/> |要求 (共有への招待の種類も) を受け入れる共有応答。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> クライアント間でメールボックスフォルダーを共有します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

