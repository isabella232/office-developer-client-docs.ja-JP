---
title: PidTagViewsEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1980e3bd815b370f125f4449dd7b7f340a7dcb9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803657"
---
# <a name="pidtagviewsentryid-canonical-property"></a>PidTagViewsEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ユーザー定義ビュー] フォルダーのエントリ id が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_VIEWS_ENTRYID  <br/> |
|識別子:  <br/> |0x35E5  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>備考

共通のフォルダー ビューにはには、フォルダーのビューには、メッセージングのユーザーによって定義された指定子が含まれているときに標準のビューの指定子の定義済みセットが含まれています。 表示指定子が多く、各メッセージとして格納されているこれらのフォルダーは、個人間メッセージ (IPM) の階層構造で表示されていないを保持できます。 指定子のセットの 2 つをマージして両方使用できるようにするクライアント アプリケーションを選択できます。
  
## <a name="related-resources"></a>関連リソース

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
