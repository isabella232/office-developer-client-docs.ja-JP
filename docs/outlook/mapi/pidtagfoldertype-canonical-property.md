---
title: PidTagFolderType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6427d6a736896e5103b2b73e0a688ced2760b84b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620241"
---
# <a name="pidtagfoldertype-canonical-property"></a>PidTagFolderType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの種類を示す定数を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLDER_TYPE  <br/> |
|識別子:  <br/> |0x3601  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のいずれかの値を指定できます。
  
FOLDER_GENERIC 
  
> メッセージおよび他のフォルダーを含む汎用フォルダー。
    
FOLDER_ROOT 
  
> フォルダー階層テーブルのルート フォルダー、つまり親フォルダーがないフォルダー。
    
FOLDER_SEARCH 
  
> 検索条件を満たすメッセージへのリンクの形式で、検索の結果を含むフォルダー。
    
メッセージ ストアのルートは、そのストア内の対人間メッセージ (IPM) サブツリーのルートと混同しないでください。 親がないストアのルート フォルダーは、NULL エントリ識別子を使用して [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出すことによって取得されます。 親を持つ IPM サブツリーのルート フォルダーは **、OpenEntry** 呼び出しに **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)プロパティの値を使用して取得されます。 
  
MAPI では、メッセージ ストアごとに 1 つのルート フォルダーのみを許可します。 このフォルダーには、メッセージと他のフォルダーが含まれます。 ルート フォルダー **PR_PARENT_ENTRYID** のプロパティ [(PidTagParentEntryId) プロパティ ( PidTagParentEntryId](pidtagparententryid-canonical-property.md)) には、フォルダーの独自のエントリ識別子が含まれる。
  
検索結果フォルダー内の情報は、主にコンテンツ テーブルに格納され、一般的なコンテンツ テーブルと同じ列と、各メッセージが見つかったフォルダーを識別する 2 つの追加列 **(PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (表示名、必須) とこのプロパティ (エントリ識別子、省略可能) が格納されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
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

