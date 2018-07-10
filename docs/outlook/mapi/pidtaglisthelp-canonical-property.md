---
title: PidTagListHelp の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7a9a5d090babce8105fab43bf8401448373777cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802957"
---
# <a name="pidtaglisthelp-canonical-property"></a>PidTagListHelp の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
多目的インターネット メール拡張 (MIME) メッセージの一覧ヘルプ ヘッダー フィールドの値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_LIST_HELP、PR_LIST_HELP_A、PR_LIST_HELP_W  <br/> |
|識別子:  <br/> |0x1043  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>備考

リスト ヘルプ ヘッダー フィールドを生成するには、クライアントは、目的の値を**PR_LIST_HELP**または関連付けられたプロパティの値を設定する必要があります。 MIME ライターは、リスト ヘルプ ヘッダー フィールドにこの値をコピーする必要があります。 
  
これらの一覧のサーバーに関連するプロパティの値を設定するのには MIME クライアントは次の表で指定されているヘッダー フィールドを書き込む必要があります。
  
|**プロパティ**|**優先のヘッダ ・ フィールド名**|**別のヘッダ ・ フィールド名**|
|:-----|:-----|:-----|
|**PR_LIST_HELP** <br/> |リスト ヘルプ  <br/> |X のヘルプ一覧  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
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
