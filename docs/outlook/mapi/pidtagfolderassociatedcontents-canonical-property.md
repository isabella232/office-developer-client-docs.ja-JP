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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316304"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a>PidTagFolderAssociatedContents 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
関連付けられたコンテンツ テーブルに関する情報を提供する埋め込みコンテンツ テーブル オブジェクトが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_FOLDER_ASSOCIATED_CONTENTS  <br/> |
|識別子:  <br/> |0x3610  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

関連付けられたコンテンツ テーブルは、標準コンテンツ テーブルに表示されないサブフォルダーを表します。 フォルダーに関連付けられているメッセージまたは非表示のメッセージが含まれます。 
  
このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。 型の **プロパティとして**、PT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。その内容は [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドによってアクセスされ、インターフェイス識別子IID_IMAPITable **要求されます** 。 サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合は、必要に応じて報告する場合があります。 
  
テーブルの内容を取得するには、クライアント アプリケーションが [IMAPIContainer::GetContentsTable メソッドを呼び出す必要](imapicontainer-getcontentstable.md) があります。 フォルダーコンテンツ テーブルの詳細については、「コンテンツ テーブル」および「 [フォルダー](contents-tables.md) [コンテンツ テーブルの表示」を参照してください](displaying-a-folder-contents-table.md)。 
  
この **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) 、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) であり、このプロパティは使用法で似ています。 複数の MAPI プロパティを使用すると、テーブルにアクセスできます。 
  
|**Property**|**表**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |コンテンツ テーブル  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |階層テーブル  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** <br/> |関連付けられたコンテンツ テーブル  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |添付ファイルテーブル  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |受信者テーブル  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議アイテムの間で変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagAssociatedContentCount 標準プロパティ](pidtagassociatedcontentcount-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

