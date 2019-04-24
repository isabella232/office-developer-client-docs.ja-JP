---
title: PidTagFolderType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316318"
---
# <a name="pidtagfoldertype-canonical-property"></a>PidTagFolderType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの種類を示す定数が格納されています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLDER_TYPE  <br/> |
|識別子:  <br/> |0x3601  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、次のいずれかの値を指定できます。
  
FOLDER_GENERIC 
  
> メッセージおよびその他のフォルダーが格納されている汎用フォルダー。
    
FOLDER_ROOT 
  
> フォルダー階層テーブルのルートフォルダーです。つまり、親フォルダーがないフォルダーです。
    
FOLDER_SEARCH 
  
> 検索条件を満たすメッセージへのリンクの形式で、検索結果を含むフォルダー。
    
メッセージストアのルートを、そのストア内の個人間メッセージ (IPM) サブツリーのルートと混同しないようにする必要があります。 親を持たないストアのルートフォルダーは、null エントリ識別子を使用して[IMsgStore:: openentry](imsgstore-openentry.md)メソッドを呼び出すことによって取得されます。 親を持つ IPM サブツリーのルートフォルダーは、 **openentry**呼び出しの**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティの値を使用して取得されます。 
  
MAPI では、メッセージストアごとに1つのルートフォルダーしか許可しません。 このフォルダーには、メッセージとその他のフォルダーが含まれています。 ルートフォルダーの**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) プロパティには、フォルダー自身のエントリ識別子が含まれています。
  
検索結果フォルダー内の情報は、主に contents テーブルと同じ列を含む contents テーブルに格納されます。また、各メッセージが見つかったフォルダーを示す2つの列もあります。 **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (表示名、必須) およびこのプロパティ (エントリ識別子、省略可能)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

