---
title: PidTagObsoletedMessageIds 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObsoletedMessageIds
api_type:
- HeaderDef
ms.assetid: bc979398-f1ad-4496-b982-428b95719369
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1f00a57798b03edb368fb0dc59fead7a2e9f5c8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416112"
---
# <a name="pidtagobsoletedmessageids-canonical-property"></a>PidTagObsoletedMessageIds 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このメッセージに取ってかえされるメッセージの識別子が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_OBSOLETED_IPMS  <br/> |
|識別子:  <br/> |0x001F  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティに含まれる識別子は、標準の検索キーで、PR_SEARCH_KEY **(** [PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティの形式を使用します。
  
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

