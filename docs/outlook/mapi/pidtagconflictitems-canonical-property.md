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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ff428d96de40e70e63659c5a3e5fa1c7cf0d564
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569114"
---
# <a name="pidtagconflictitems-canonical-property"></a>PidTagConflictItems 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
1 つまたは複数のエントリが自動競合解決に関係している項目の Id が含まれています。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|識別子:  <br/> |0x1098  <br/> |
|プロパティの種類:  <br/> |PT_MV_BINARY  <br/> |
|領域:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>注釈

自動競合の解決をサポートする標準の Outlook アイテムの種類には、次の標準的な項目の種類が含まれます: 予定表アイテム、連絡先アイテム、履歴項目、メール アイテム、会議アイテム、付箋項目、および作業項目です。 これらの標準的な項目の種類のいずれかから派生したメッセージ クラスに属するアイテムが自動競合の解決をサポートします。 Microsoft Outlook 2003 と Microsoft Office Outlook 2007 では、Outlook がアイテムを同期し、結果のコピーにすべての重要なデータが含まれていない可能性があります可能性があることを考慮すると Outlook コピーが格納されて、競合している**競合****同期の失敗**フォルダーの下のフォルダーです。 
  
> [!NOTE]
> [**移動**] メニューの**フォルダー一覧**をクリックするまで、**同期の問題**とそのサブフォルダーは表示されません。 
  
自動競合解決をサポートしている項目の種類の 1 つ、競合の解決では、受注、または、競合の解決のため、[**競合**] フォルダーに格納された場合、アイテムは、 **PR_CONFLICT_ITEMS**プロパティを公開します。 アイテムが置かれているフォルダーでは、 **PR_CONFLICT_ITEMS**の内容を決定します。 アイテムに競合の解決を獲得する必要がありますが、 **PR_CONFLICT_ITEMS**の 1 つまたは複数のエントリ Id が含まれることの項目は、[**競合**] フォルダー以外のフォルダー内にあるアイテムは、 **PR_CONFLICT_ITEMS**プロパティを公開する場合は、競合の解決で失われたそれらのアイテムです。 項目は、[**競合**] フォルダー内にあるアイテムは、 **PR_CONFLICT_ITEMS**プロパティを公開する場合は、この項目が競合の解決、失われている必要があり、競合に勝利するアイテムのエントリ ID に含まれることには、 **PR_CONFLICT_ITEMS**解像度です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI の追加について](about-mapi-additions.md)
  
[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

