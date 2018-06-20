---
title: PidTagOriginallyIntendedRecipAddrtype の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipAddrtype
api_type:
- COM
ms.assetid: dcfb6bd5-bff5-4a50-aec7-4bdfdabf7631
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ddb2a246ca77f751ddd428941cd16da6aa5e286b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803093"
---
# <a name="pidtagoriginallyintendedrecipaddrtype-canonical-property"></a>PidTagOriginallyIntendedRecipAddrtype の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
自動転送されたメッセージの最初の目的の受信者のアドレスの種類が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_A、PR_ORIGINALLY_INTENDED_RECIP_ADDRTYPE_W  <br/> |
|識別子:  <br/> |0x007B  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、本来意図されているメッセージの受信者のアドレスのプロパティの 1 つです。 メッセージを転送するには、自動でエージェントを設定しなければなりません。
  
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

