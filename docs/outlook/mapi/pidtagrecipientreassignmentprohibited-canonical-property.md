---
title: PidTagRecipientReassignmentProhibited 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341112"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>PidTagRecipientReassignmentProhibited 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
電子メール メッセージに対して、メッセージを転送するときに受信者を追加することを禁止するかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|識別子:  <br/> |0x002B  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、電子メール メッセージの値 ([PidTagSensitivity](pidtagsensitivity-canonical-property.md) **)** PR_SENSITIVITYに基づいて設定されます。 PR_SENSITIVITYが "0x00000000" (標準) または "0x00000003" (機密) に設定されている場合、このプロパティを "0x00" に設定するか、電子メール メッセージに別の受信者を追加できます。 電子メール オブジェクトの **PR_SENSITIVITY** が "0x00000001" (個人用) または "0x00000002" (プライベート) に設定されている場合、転送によってこのメールの受信者が追加または異なって追加されるのを防ぐために、このプロパティを "0x01" に設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

