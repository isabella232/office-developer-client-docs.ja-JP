---
title: PidTagContentUnreadCount の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ce7092840037345ae99b31c39cfbd4ac96b99ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802624"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>PidTagContentUnreadCount の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ ・ ストアによって計算される、フォルダー内の未読メ ッ セージの数が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONTENT_UNREAD  <br/> |
|識別子:  <br/> |0x3603  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>備考

関連は、目的が異なる、2 つのメッセージ ・ ストアによって計算されるこのプロパティが使用されます。 MAPI フォルダーのオブジェクトでは、フォルダー内のメッセージの数が含まれます。 カテゴリ別の MAPI テーブル内の見出し行には見出し行に対応するカテゴリ内の関連付けられていない未読メ ッ セージの数が含まれています。
  
このプロパティには、対象の MSGFLAG_READ フラグを**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティで設定しないフォルダー コンテンツ テーブル内のメッセージの数が含まれています。 **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) のプロパティには、フォルダーのメッセージの合計数が含まれています。 **PR_CONTENT_COUNT**し、このプロパティは、クライアントには読み取り専用です。 
  
一部のクライアント アプリケーションは、このプロパティの値により異なる方法でカテゴリの見出し行を表示します。 たとえば、クライアントでは、太字で未読メ ッ セージを含むカテゴリを表示できます。 このプロパティは、MAPI_E_INVALID_PARAMETER 値は、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドから返されるように分類しようとすると使用できません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダーの操作を処理します。
    
[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> テーブルのコア オブジェクトに許容される操作が含まれます。
    
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

