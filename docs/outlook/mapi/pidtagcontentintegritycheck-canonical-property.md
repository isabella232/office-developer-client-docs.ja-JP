---
title: PidTagContentIntegrityCheck 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a627e39b3502fcba0d9657d6562b6745e06077f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555483"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>PidTagContentIntegrityCheck 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ送信者が未承認の受信者への開示からメッセージコンテンツを保護できる ASN.1 コンテンツ整合性チェック値を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|識別子:  <br/> |0x0C00  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージ コンテンツの否認不可を提供します。 メッセージ **のPR_MESSAGE_TOKEN** [(PidTagMessageToken)](pidtagmessagetoken-canonical-property.md)と組み合わせて、メッセージの内容が変更されずに宛先に到着します。
  
## <a name="related-resources"></a>関連リソース

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

