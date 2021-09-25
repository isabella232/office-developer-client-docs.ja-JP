---
title: PidTagMemberEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 851c08abcb1d75d6649bb9b5f46618ffa4500d0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609860"
---
# <a name="pidtagmemberentryid-canonical-property"></a>PidTagMemberEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
システム アクセス制御リスト (SACL) テーブル メンバーのディレクトリ オブジェクトエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MEMBER_ENTRYID  <br/> |
|識別子:  <br/> |0x0FFF  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、IExchangeModifyTable](iexchangemodifytableiunknown.md) インターフェイスで使用して、SACL が適用されるユーザーまたは役割を一意に識別します。 SACL テーブルでメンバーを作成した後 **、ENTRYID を** 変更することはできません。 変更するには、テーブル メンバーを削除し、別の ENTRYID を使用してテーブル メンバーを **再作成する必要があります**。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

