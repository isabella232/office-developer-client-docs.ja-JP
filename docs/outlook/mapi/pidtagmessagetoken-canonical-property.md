---
title: PidTagMessageToken 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7357b7b98d90d08f7d14e965458703e4e193f63a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803000"
---
# <a name="pidtagmessagetoken-canonical-property"></a>PidTagMessageToken 標準プロパティ

  
  
**適用対象**: Outlook 
  
メッセージを ASN.1 にセキュリティ トークンが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_TOKEN  <br/> |
|識別子:  <br/> |0x0C03  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージング プロパティをセキュリティで保護します。  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、保護されているセキュリティに関連する情報の発信者から受信者を伝達します。 **PR_MESSAGE_SECURITY_LABEL** ([PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) のプロパティと組み合わせて、メッセージの内容とラベルの関連付けを保証します。 **PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck](pidtagcontentintegritycheck-canonical-property.md)) のプロパティと組み合わせて、メッセージの内容が変更されていないことを確認します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

