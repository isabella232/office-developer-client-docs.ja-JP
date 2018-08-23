---
title: PidTagFolderAssociatedContents 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ae09488b99cd55e5cfca23f504d81ac5919633d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574154"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a>PidTagFolderAssociatedContents 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
コンテンツが関連付けられているテーブルに関する情報を提供する埋め込まれたコンテンツ テーブル オブジェクトが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLDER_ASSOCIATED_CONTENTS  <br/> |
|識別子:  <br/> |0x3610  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>注釈

コンテンツが関連付けられているテーブルでは、標準的な内容の表に表示されていないサブフォルダーを表します。 フォルダーの関連する、または非表示、メッセージが含まれています。 
  
このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。 **PT_OBJECT**の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **IID_IMAPITable**のインタ フェース識別子を要求するその内容にアクセスする必要があります。 サービス プロバイダーする必要があります報告して[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを報告ことがあります (オプション) が設定されている場合、またはに設定されていない場合はありません。 
  
テーブルの内容を取得するには、クライアント アプリケーションは、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出す必要があります。 フォルダーの内容のテーブルの詳細については、[テーブルの内容](contents-tables.md)と[フォルダーの内容のテーブルを表示する](displaying-a-folder-contents-table.md)を参照してください。 
  
**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))、このプロパティは、使用状況に似ています。 いくつかの MAPI プロパティは、テーブルへのアクセスを提供します。 
  
|**プロパティ**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |コンテンツ テーブル  <br/> |
|**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |階層テーブル  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** <br/> |関連付けられているコンテンツ」テーブル  <br/> |
|**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |添付ファイル テーブル  <br/> |
|**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |受信者テーブル  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議アイテムに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagAssociatedContentCount 標準プロパティ](pidtagassociatedcontentcount-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

