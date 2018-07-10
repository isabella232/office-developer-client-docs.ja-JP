---
title: PidTagAccessControlListTable の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d992c7ac43c736e01184e1f12b3ad366587c9b06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802398"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>PidTagAccessControlListTable の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
すべてのシステム アクセス制御リスト (SACL) のフォルダーに適用されるので構成されるテーブルが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ACL_TABLE  <br/> |
|識別子:  <br/> |0x3FE0  <br/> |
|データを入力します。  <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |アクセス制御  <br/> |
   
## <a name="remarks"></a>備考

このプロパティでは、Exchange Server 上のすべてのフォルダー オブジェクト上に存在します。 値がこのプロパティに含まれているは、読み取り用に使用され、フォルダーのリスト (Acl) のアクセス制御を変更します。 **IID_IExchangeModifyTable**インターフェイス識別子を使用して[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを使用するにを取得するのには、 [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)フォルダーの ACL テーブルへのインターフェイスです。 読み取りおよびそれらの Acl を変更するには、このインターフェイスを使用します。 
  
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
