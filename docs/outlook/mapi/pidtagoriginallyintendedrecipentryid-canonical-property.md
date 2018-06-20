---
title: PidTagOriginallyIntendedRecipEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEntryId
api_type:
- COM
ms.assetid: fc288a7a-1927-484e-b860-9cc118672ed2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4745318d5666cc3c138f424c94bc2c5e430a61d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803066"
---
# <a name="pidtagoriginallyintendedrecipentryid-canonical-property"></a>PidTagOriginallyIntendedRecipEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
自動転送メッセージの最初の目的の受信者のエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ENTRYID  <br/> |
|識別子:  <br/> |0x1012  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、本来意図されているメッセージの受信者のアドレスのプロパティのいずれかです。 メッセージを転送するには、自動でエージェントを設定しなければなりません。
  
このプロパティは、レポートの X.400 受信者ごとの属性に対応します。
  
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

