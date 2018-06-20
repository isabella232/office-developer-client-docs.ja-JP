---
title: PidNameContentBase の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 21469b944bb2ce5db0576e40012335d89d48cb49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802359"
---
# <a name="pidnamecontentbase-canonical-property"></a>PidNameContentBase の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
[RFC3282] 内容ベース ヘッダー フィールドの値が含まれています。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |BodyContentBase  <br/> |
|プロパティを設定します。  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |コンテンツ ・ ベース  <br/> |
|データを入力します。  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値を設定するのには多目的インターネット メッセージの拡張機能 (MIME) クライアントに書き込まなければなりません目的の値内容ベース ヘッダー フィールドにメッセージの本文にマップされた MIME エンティティ。 MIME のリーダーは、このプロパティの値をこのような MIME エンティティのコンテンツ ベースのヘッダー フィールドの値をコピーする必要があります。
  
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

