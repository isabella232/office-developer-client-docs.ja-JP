---
title: PidTagCommonViewsEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d4d4de75d6d001584ea5cd6d833dc85f12913081
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600401"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>PidTagCommonViewsEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
定義済みの共通ビュー フォルダーのエントリ識別子を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|識別子:  <br/> |0x35E6  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Outlookアプリケーション  <br/> |
   
## <a name="remarks"></a>注釈

共通ビュー フォルダーには定義済みの標準ビュー指定子のセットが含まれる一方、ビュー フォルダーにはメッセージング ユーザーによって定義された指定子が含まれる。 これらのフォルダーは、対人間メッセージ (IPM) 階層には表示されませんが、多くのビュー指定子を保持できます。各フォルダーはメッセージとして保存されます。 クライアント アプリケーションは、2 つの指定子セットを結合し、両方を使用できます。 
  
ビューの詳細については、「フォルダーの表示」 [を参照してください](mapi-view-folders.md)。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagDefaultViewEntryId 標準プロパティ](pidtagdefaultviewentryid-canonical-property.md)
  
[PidTagViewsEntryId 標準プロパティ](pidtagviewsentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

