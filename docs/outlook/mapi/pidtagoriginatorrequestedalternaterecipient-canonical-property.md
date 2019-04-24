---
title: PidTagOriginatorRequestedAlternateRecipient 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 45cd0e8a95f908d7ef56d03b3ecab5d5df5bcae1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342001"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a>PidTagOriginatorRequestedAlternateRecipient 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信者によって指定された代替受信者のエントリ識別子を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT  <br/> |
|識別子:  <br/> |0x0c09  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、autoforwarded メッセージで使用されます。 自動転送が許可されていない場合、または代替受信者が指定されていない場合は、配信不能レポートを生成する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

