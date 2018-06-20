---
title: PidTagContentIntegrityCheck の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentIntegrityCheck
api_type:
- HeaderDef
ms.assetid: c7f10b8a-6b20-44cf-bde6-8d2b711c1c14
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2082db4ccd107fcd02e37882707e4e3ee697695d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802612"
---
# <a name="pidtagcontentintegritycheck-canonical-property"></a>PidTagContentIntegrityCheck の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
漏えいから不正な受信者にメッセージの内容を保護するためにメッセージの送信者を許可する ASN.1 のコンテンツの整合性チェック値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONTENT_INTEGRITY_CHECK  <br/> |
|識別子:  <br/> |場合は 0x0c00。  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージのコンテンツの否認を提供します。 **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) と協力して、メッセージの内容がそのまま目的地に到着することが保証されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

