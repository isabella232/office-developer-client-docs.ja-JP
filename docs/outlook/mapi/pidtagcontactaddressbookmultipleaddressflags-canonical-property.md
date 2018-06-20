---
title: PidTagContactAddressBookMultipleAddressFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fbe955d3e7a509edf6ba10678e1e2538c9185193
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802562"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlags の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
連絡先アイテムごとでは、プロバイダーが複数の電子メールをサポートするかどうかを示すフラグが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|識別子:  <br/> |0x6625  <br/> |
|データを入力します。  <br/> |PT_MV_LONG  <br/> |
|領域:  <br/> |連絡先のアドレス帳  <br/> |
   
## <a name="remarks"></a>備考

このプロパティのフラグが TRUE の場合は、プロバイダーでは、この電子メール アドレスがない連絡先は含まれません。 プライマリ電子メール アドレスのみが受け入れられます。 これは、アドレス帳の連絡先のプロファイル セクションのプロパティです。
  
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

