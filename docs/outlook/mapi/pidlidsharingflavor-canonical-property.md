---
title: PidLidSharingFlavor 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327483"
---
# <a name="pidlidsharingflavor-canonical-property"></a>PidLidSharingFlavor 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
共有メッセージのプロパティとして指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidsharingflavor  <br/> |
|プロパティセット:  <br/> |PSETID_Sharing  <br/> |
|ロング ID (LID):  <br/> |0x00008a18  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値は、次のいずれかであることが必要です。
  
|**値**|**共有メッセージオブジェクトの種類**|
|:-----|:-----|
|0x00020310  <br/> |特別なフォルダーの共有への招待。  <br/> |
|0x00000310  <br/> |特別なフォルダーではないフォルダーの共有への招待。  <br/> |
|0x00020500  <br/> |共有の依頼。  <br/> |
|0x00020710  <br/> |特別なフォルダーの共有への招待と、受信者の同等の特殊フォルダーに対する共有要求の両方。  <br/> |
|0x00025100  <br/> |要求を拒否する共有応答。  <br/> |
|0x00023310  <br/> |要求 (共有への招待の種類も) を受け入れる共有の応答。  <br/> |
   
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

