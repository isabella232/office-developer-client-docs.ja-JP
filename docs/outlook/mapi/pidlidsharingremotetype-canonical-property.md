---
title: PidLidSharingRemoteType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteType
api_type:
- COM
ms.assetid: e9bc7c7c-86df-45d8-922b-76e3b076144a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3297ca951097c9f3601086809c6e294854c88656
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331212"
---
# <a name="pidlidsharingremotetype-canonical-property"></a>PidLidSharingRemoteType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リモート共有フォルダーの種類を指定します。 これは、共有メッセージのプロパティです。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidsharingremotetype  <br/> |
|プロパティセット:  <br/> |PSETID_Sharing  <br/> |
|ロング ID (LID):  <br/> |0x00008a1d  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、 **dispidsharinglocaltype** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) プロパティと同じ値に設定する必要があります。無視する必要があります。
  
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

