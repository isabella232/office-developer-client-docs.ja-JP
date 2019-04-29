---
title: PidTagMessageSecurityLabel 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b6900cbacc2bea6c5519efdc4281ca98629b23bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425674"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a>PidTagMessageSecurityLabel 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージのセキュリティラベルが保存されています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_SECURITY_LABEL  <br/> |
|識別子:  <br/> |0x001e  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |サーバー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、 **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) プロパティがメッセージを保護する基準を指定します。 メッセージコンテンツとの関連付けは、トークンによって保証されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

