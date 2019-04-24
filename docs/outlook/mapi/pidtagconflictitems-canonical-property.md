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
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338018"
---
# <a name="pidtagconflictitems-canonical-property"></a>PidTagConflictItems 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
競合の自動解決に関係しているアイテムの1つ以上のエントリ id を含みます。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONFLICT_ITEMS  <br/> |
|識別子:  <br/> |0x1098  <br/> |
|プロパティの種類:  <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |ICS  <br/> |
   
## <a name="remarks"></a>解説

自動競合解決をサポートする標準の Microsoft Outlook アイテムの種類には、予定アイテム、連絡先アイテム、ジャーナルアイテム、メールアイテム、会議アイテム、付箋アイテム、およびタスクアイテムの標準のアイテムの種類があります。 このような標準アイテムの種類のいずれかから派生するメッセージクラスに属するアイテムは、競合の自動解決もサポートします。 microsoft outlook 2003 および microsoft Office outlook 2007 では、outlook がアイテムを同期し、結果コピーに重要なデータがまったく含まれていない可能性があると判断した場合、**競合**するコピーを outlook に格納します。フォルダーを、[**同期の失敗**] フォルダーにします。 
  
> [!NOTE]
> **同期の問題**とそのサブフォルダーは、[**移動**] メニューの [**フォルダー一覧**] をクリックするまで表示されません。 
  
アイテムは、自動競合解決をサポートしているアイテムの種類のいずれか、競合の解決に勝ち、競合の解決によって [**競合**] フォルダーに配置されたアイテムの**PR_CONFLICT_ITEMS**プロパティを公開します。 **PR_CONFLICT_ITEMS**のコンテンツは、アイテムが配置されるフォルダーによって決まります。 アイテムが**競合**フォルダー以外のフォルダーに配置されていて、アイテムが**PR_CONFLICT_ITEMS**プロパティを公開している場合、アイテムは競合の解決を獲得する必要があり、 **PR_CONFLICT_ITEMS**には1つ以上のエントリ id が含まれます。競合の解決で失われたアイテム。 アイテムが conflict フォルダーに配置さ**** れていて、アイテムが**PR_CONFLICT_ITEMS**プロパティを公開している場合、このアイテムは競合の解決を失い、 **PR_CONFLICT_ITEMS**には競合に勝ったアイテムのエントリ ID が格納されます。画質. 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI の追加について](about-mapi-additions.md)
  
[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

