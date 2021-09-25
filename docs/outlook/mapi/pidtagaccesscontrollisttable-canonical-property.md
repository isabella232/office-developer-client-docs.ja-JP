---
title: PidTagAccessControlListTable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 494a767f08d6ba473ef3260daff5fc122d2926a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563967"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>PidTagAccessControlListTable 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーに適用されるすべてのシステム アクセス制御リスト (SACL) で構成されるテーブルを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACL_TABLE  <br/> |
|識別子:  <br/> |0x3FE0  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |アクセス制御  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、フォルダー上のすべてのフォルダー オブジェクトExchange Server。 このプロパティに含まれる値は、フォルダーのアクセス制御リスト (ACL) の読み取りおよび変更に使用されます。 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを **IID_IExchangeModifyTable** インターフェイス識別子と一緒に使用して [、IExchangeModifyTable : フォルダー](iexchangemodifytableiunknown.md)の ACL テーブルへの IUnknown インターフェイスを取得できます。 このインターフェイスを使用して、これらの ACL を読み取り、変更できます。 
  
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

