---
title: PidTagContactAddressBookMultipleAddressFlag の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802573"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlag の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
連絡先アイテムごとに複数の電子メール アドレスをプロバイダーがサポートする場合は TRUE にするフラグが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|識別子:  <br/> |0x6614  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |連絡先のアドレス帳  <br/> |
   
## <a name="remarks"></a>備考

このプロパティが TRUE の場合、プロバイダーは電子メール アドレスがない連絡先を許可しません。 FALSE の場合、プロバイダーは、通常の電子メール アドレスがあるかどうかすべての連絡先を示します。 プライマリ電子メール アドレスのみが受け入れられます。 これは、連絡先のアドレス帳コンテナー、および連絡先のアドレス帳コンテナーのテーブル内の列のプロパティです。
  
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

