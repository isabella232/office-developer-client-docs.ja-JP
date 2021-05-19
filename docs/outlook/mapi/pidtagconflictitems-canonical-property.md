---
title: PidTagConflictItems 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338018"
---
# <a name="pidtagconflictitems-canonical-property"></a>PidTagConflictItems 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
自動競合解決に関与したアイテムの 1 つ以上のエントリの ID を含む。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|識別子:  <br/> |0x1098  <br/> |
|プロパティの種類:  <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>注釈

自動競合解決をサポートする標準の Microsoft Outlook アイテムの種類には、予定アイテム、連絡先アイテム、ジャーナル アイテム、メール アイテム、会議アイテム、付箋アイテム、タスク アイテムの標準アイテムの種類が含まれます。 これらの標準アイテムの種類の 1 つから派生するメッセージ クラスに属するアイテムは、自動競合解決もサポートします。 Microsoft Outlook 2003 および Microsoft Office Outlook 2007 では、Outlook がアイテムを同期し、結果のコピーにすべての重要なデータが含まれている可能性があると考える場合、Outlook は競合するコピーを [同期の問題] フォルダーの[競合] フォルダーに格納します。 
  
> [!NOTE]
> **[移動] メニューの**[フォルダー一覧]をクリックするまで、同期の問題とそのサブフォルダー **は非表示** になります。 
  
自動競合解決をサポートするアイテムの種類の 1 つ、競合解決で勝ったアイテム、または競合解決のために **Conflicts** フォルダーに配置されている場合、アイテムは **PR_CONFLICT_ITEMS** プロパティを公開します。 アイテムを配置するフォルダーによって、アイテムのコンテンツが **PR_CONFLICT_ITEMS。** アイテムが **Conflicts** フォルダー以外の一部のフォルダーにあり、 **そのアイテム** が PR_CONFLICT_ITEMS プロパティを公開している場合、そのアイテムは競合解決に勝っている必要があります **。PR_CONFLICT_ITEMS** には、競合解決で失われたアイテムの 1 つ以上のエントリの ID が含まれます。 アイテムが **Conflicts** フォルダーにあり、アイテムが **PR_CONFLICT_ITEMS** プロパティを公開している場合、このアイテムは競合解決を失い **、PR_CONFLICT_ITEMS** には競合解決で勝ったアイテムのエントリ ID が含まれている必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI の追加について](about-mapi-additions.md)
  
[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

