---
title: PidLidSharingCapabilities 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d44851e1c863cb117eed3462eb98de87f8d1f0be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358892"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a>PidLidSharingCapabilities 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
共有メッセージのプロパティとして指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidSharingCaps  <br/> |
|プロパティ セット:  <br/> |PSETID_Sharing  <br/> |
|長い ID (LID):  <br/> |0x00008A17  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |共有  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、次のいずれかの値に設定する必要があります。
  
|**値**|**シナリオ**|
|:-----|:-----|
|0x00040290  <br/> |この共有メッセージ オブジェクトは、特別なフォルダーに関連付きます。  <br/> |
|0x000402B0  <br/> |この共有メッセージ オブジェクトは、特別なフォルダーには関連付けされません。  <br/> |
   
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

