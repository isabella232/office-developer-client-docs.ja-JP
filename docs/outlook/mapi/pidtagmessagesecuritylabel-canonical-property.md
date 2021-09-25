---
title: PidTagMessageSecurityLabel 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6b83c36c18adf4bdf027bf9b4d1c677a30efee13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599918"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a>PidTagMessageSecurityLabel 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージのセキュリティ ラベルが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_SECURITY_LABEL  <br/> |
|識別子:  <br/> |0x001E  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |サーバー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、PR_MESSAGE_TOKEN **(** [PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) プロパティがメッセージを保護する基礎を提供します。 メッセージ コンテンツとの関連付けは、トークンによって保証されます。
  
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

