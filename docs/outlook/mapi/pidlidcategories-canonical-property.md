---
title: PidLidCategories の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801840"
---
# <a name="pidlidcategories-canonical-property"></a>PidLidCategories の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
アイテムのカテゴリの一覧を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidCategories  <br/> |
|プロパティを設定します。  <br/> |PS_PUBLIC_STRINGS  <br/> |
|長い ID (LID):  <br/> |0x00002328  <br/> |
|データを入力します。  <br/> |PT_MV_UNICODE  <br/> |
|領域:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>備考

キーワード ヘッダー フィールドを生成するには、クライアントは、目的の値にこのプロパティの値を設定する必要があります。 このプロパティは、複数の文字列です。各カテゴリは、1 つのキーワードにマップする必要があります。
  
多目的インターネット メール拡張 (MIME) の作成者は、[キーワード] ヘッダー フィールドの (U + 002 C) コンマとスペース (U + 0020) に分離することで別のキーワードをこのプロパティの各部分の値をコピーする必要がありますそれぞれのキーワードです。 MIME ライターは、さまざまな組織内のカテゴリの別のセットの間に競合を避けるために、[キーワード] ヘッダー フィールドにコピーすることではなく、このプロパティを削除可能性があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

