---
title: PidTagRelatedMessageIds 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRelatedMessageIds
api_type:
- COM
ms.assetid: 51f0eb8a-0a16-4b45-9380-28caddecf955
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 501b5e6acc83a5da27af3ef6024ecc9e049893cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624623"
---
# <a name="pidtagrelatedmessageids-canonical-property"></a>PidTagRelatedMessageIds 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが関連付けされているメッセージの識別子の一覧が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RELATED_IPMS  <br/> |
|識別子:  <br/> |0x002D  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

識別子は、プロパティ ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティで使用されるのと同PR_SEARCH_KEY特定 **の** 構築ルールを使用します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

