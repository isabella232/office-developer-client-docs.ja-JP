---
title: PidTagContainerContents 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283129"
---
# <a name="pidtagcontainercontents-canonical-property"></a>PidTagContainerContents 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーに関する情報を提供する埋め込みコンテンツ テーブル オブジェクトを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAINER_CONTENTS  <br/> |
|識別子:  <br/> |0x360F  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。 型のプロパティPT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。その内容は [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドによってアクセスされ、インターフェイス識別子IID_IMAPITableする必要があります。 サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合はオプションで報告できます。 
  
テーブルの内容を取得するには、クライアント アプリケーションが [IMAPIContainer::GetContentsTable メソッドを呼び出す必要](imapicontainer-getcontentstable.md) があります。 詳細については、「コンテンツ テーブル [」を参照してください](contents-tables.md)。 
  
このプロパティは **、PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) 、および **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) の使用法と似ています。 複数の MAPI プロパティを使用すると、テーブルにアクセスできます。 
  
|**Property**|**表**|
|:-----|:-----|
|PidTagContainerContents  <br/> |コンテンツ テーブル  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |階層テーブル  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |関連付けられたコンテンツ テーブル  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |添付ファイルテーブル  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |受信者テーブル  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

