---
title: PidTagSearchRecipientEmailTo の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5d6c029ba91b6b3489d3f6544ead6788760363a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803497"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a>PidTagSearchRecipientEmailTo の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
照会中の電子メール アドレスまたはストア内のメッセージの [**宛先**] 行でアドレス指定された受信者の表示名の一覧で、Unicode 文字列が含まれています。 
  
## 

|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SEARCH_RECIP_EMAIL_TO_W  <br/> |
|識別子:  <br/> |0x0EA6  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |検索  <br/> |
   
## <a name="related-resources"></a>関連リソース

> [!NOTE]
> この MAPI 制限のタグ、電子メール アドレスを検索または表示名のメッセージを送信するときに使用しない現在あるダウンロード可能なヘッダー ファイルで定義できます。 次の値を使用して、コードに追加できます >。`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`
  
### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。
    
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

