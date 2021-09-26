---
title: PidTagContainerHierarchy 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 65460c148c812793b72220e3d2b2bba6ccd227ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583535"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>PidTagContainerHierarchy 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
子コンテナーに関する情報を提供する埋め込み階層テーブル オブジェクトを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|識別子:  <br/> |0x360E  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。 型の **プロパティとして**、PT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。その内容は [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドによってアクセスされ、インターフェイス識別子IID_IMAPITableする必要があります。 サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合はオプションで報告できます。 
  
表の内容を取得するには、クライアント アプリケーションが [IMAPIContainer::GetHierarchyTable メソッドを呼び出す必要](imapicontainer-gethierarchytable.md) があります。 詳細については、「階層テーブル [」を参照してください](hierarchy-tables.md)。 
  
 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) **、PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) 、このプロパティは使用法で似ています。 複数の MAPI プロパティを使用すると、テーブルにアクセスできます。 
  
|**プロパティ**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |コンテンツ テーブル  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |階層テーブル  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |関連付けられたコンテンツ テーブル  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |添付ファイルテーブル  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |受信者テーブル  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
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

