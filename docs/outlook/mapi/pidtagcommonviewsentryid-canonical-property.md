---
title: PidTagCommonViewsEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331746"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a>PidTagCommonViewsEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
定義済みの共通ビューフォルダーのエントリ識別子を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_COMMON_VIEWS_ENTRYID  <br/> |
|識別子:  <br/> |0x35e6  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>解説

common view フォルダーには、あらかじめ定義されている標準ビュー指定セットが含まれています。ビューフォルダーには、メッセージングユーザーによって定義された指定子が含まれています。 これらのフォルダーは、個人間メッセージ (IPM) 階層では表示されず、メッセージとして格納されている複数のビュー指定子を保持できます。 クライアントアプリケーションは、2つの指定子のセットをマージすることを選択し、両方を使用できるようにします。 
  
ビューの詳細については、「 [View Folders](mapi-view-folders.md)」を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagDefaultViewEntryId 標準プロパティ](pidtagdefaultviewentryid-canonical-property.md)
  
[PidTagViewsEntryId 標準プロパティ](pidtagviewsentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

