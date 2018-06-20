---
title: PidTagFolderType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2520a7544eb4ba39cd83a7a0aa65b98bd8a67deb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802758"
---
# <a name="pidtagfoldertype-canonical-property"></a>PidTagFolderType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フォルダーの種類を示す定数が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_FOLDER_TYPE  <br/> |
|識別子:  <br/> |0x3601  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、次の値の 1 つだけ持つことができます。
  
FOLDER_GENERIC 
  
> メッセージおよびその他のフォルダーに含まれている一般的なフォルダーです。
    
FOLDER_ROOT 
  
> フォルダーの階層テーブル、つまり、親フォルダーがないフォルダーのルート フォルダーです。
    
FOLDER_SEARCH 
  
> 検索条件を満たすメッセージへのリンクの形式で、検索の結果を格納するフォルダーです。
    
メッセージ ストアのルートは、そのストア内の個人間メッセージ (IPM) サブツリーのルートと混同しないでください。 ストアのルート フォルダーは、親を持たないが null のエントリの識別子を使用して[IMsgStore::OpenEntry](imsgstore-openentry.md)メソッドを呼び出すことによって取得されます。 **OpenEntry**呼び出しの**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティの値を使用して、IPM サブツリーのルート フォルダーは、親を持っているが、取得します。 
  
MAPI は、メッセージ ・ ストアごとに 1 つだけのルート フォルダーを使用できます。 このフォルダーには、メッセージ、およびその他のフォルダーが含まれています。 ルート フォルダーの**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) のプロパティには、フォルダーのエントリ id が含まれています。
  
検索結果フォルダー内の情報がそのコンテンツ ・ テーブルの一般的な内容のテーブルと同じ列と一致する各メッセージが含まれているフォルダーを識別する 2 つの余分な列が含まれている主に格納されている: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (表示名が必要です)、このプロパティ (エントリの識別子、省略可能)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダーの操作を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

