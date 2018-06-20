---
title: PidTagContactAddressBookStoreSupportMask の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5cd113c263c97ba306fcf7bf97c750e710eac922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802579"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>PidTagContactAddressBookStoreSupportMask の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
連絡先フォルダーを含むストアから取得した**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) のプロパティが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|識別子:  <br/> |0x6611  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |連絡先のアドレス帳  <br/> |
   
## <a name="remarks"></a>備考

連絡先アドレス帳プロバイダーは、このプロパティを使用して、ストアのサポートされている機能の妥当性を評価します。 これは、連絡先のアドレス帳コンテナー、および連絡先のアドレス帳コンテナーのテーブル内の列のプロパティです。
  
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

