---
title: 階層テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 23314418836893b40cbddf3b90bd95ec061a00c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800221"
---
# <a name="hierarchy-tables"></a>階層テーブル

  
  
**適用対象**: Outlook 
  
階層テーブルには、メッセージ ・ ストア内のフォルダーまたはアドレス帳コンテナーにコンテナーに関する情報が含まれています。 階層テーブルの各行には、1 つのフォルダーまたはアドレス帳コンテナーに関する情報を持つ列のセットが含まれています。 階層テーブルは、主にクライアントによって使用されるフォルダーとサブフォルダーのツリーを表示するのには、メッセージ ストア プロバイダーによって実装され、アドレス帳コンテナーのツリーを表示するアドレス帳のプロバイダーによって実装されています。 コンテナーのサブコンテナーを保持することはできませんが、 **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) のプロパティに AB_SUBCONTAINERS フラグがない場合で示されるように実装しない階層テーブルです。
  
階層テーブルを呼び出すことによってアクセスできます。
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)。
    
    - または、
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)は、プロパティ タグとインターフェイス識別子として IID_IMAPITable として**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) を渡すことです。
    
コンテナー、フォルダーは、[表のプロパティを取得するための両方の方法をサポートしなければなりません。 どちらかを選択することがクライアントにこれらのテーブルをアクセスするための方法の 1 つのみをサポートするためにサービス ・ プロバイダーの許容可能なことはできません。 
  
> [!IMPORTANT]
> 階層テーブルの指定した並べ替え順を優先するのには、ストア プロバイダーは保証されません。 
  
**IMAPIProp::OpenProperty**への呼び出しでは、対応するプロパティ、 **PR_CONTAINER_HIERARCHY**を開いて、階層テーブルにアクセスする必要があります。 フォルダーまたはコンテナーの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを**PR_CONTAINER_HIERARCHY**を取得することはできませんが、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドによって返されるプロパティ タグ配列に含まれます。 
  
 **PR_CONTAINER_HIERARCHY**は、コピー操作の階層テーブルをエクスクルードまたはインクルードするにも使用できます。 クライアントは、コピー操作で[IMAPIProp::CopyTo](imapiprop-copyto.md)の*lpExcludeProps*パラメーターでの**PR_CONTAINER_HIERARCHY**を指定した場合、新しいフォルダーまたはコンテナーはサポートされません、元のフォルダーまたはコンテナーの階層テーブル。 
  
次のプロパティは、必要な列の階層テーブルの設定を構成します。
  
|||
|:-----|:-----|
|**PR_COMMENT**([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS**([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME**には、コンテナーまたは階層の表示に表示されるフォルダーの名前が含まれています。 
  
 **PR_ENTRYID**は、このコンテナーまたはフォルダーに関連付けられているエントリの識別子です。 長期のエントリ id を使用する予定です。 クライアントと、MAPI は、コンテナーまたはフォルダーを開き、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を呼び出すことによってその内容を表示する**OpenEntry**にこのエントリの識別子を渡すことができます。 
  
 **PR_DEPTH**は、0 が最上位レベルでこのコンテナーまたはフォルダーのインデントのレベルを示す数値です。 コンテナーまたはフォルダー階層のより深いレベルが存在する、 **PR_DEPTH**プロパティの値を大きくします。 クライアントは、ユーザーが明確に親と子の関係を確認できるように、階層テーブルを適切に表示するのには、 **PR_DEPTH**プロパティを使用します。 コンテナーまたはフォルダーの深さは常にコンテナーまたはフォルダーの階層テーブルを実装します。 
  
 **PR_OBJECT_TYPE**は常に設定 MAPI_ABCONT にアドレス帳階層テーブルおよび MAPI_FOLDER フォルダーの階層テーブルにします。 
  
 **PR_DISPLAY_TYPE**は、コンテナーまたはフォルダーの階層テーブルの表示方法に関連する数値値です。 表示用には、コンテナーまたはフォルダーの種類を視覚的に区別するために主に使用されます。 多くのメッセージは、保存し、アドレス帳プロバイダーは、さまざまな表示の種類のアイコンを使用します。 これらのアイコンを提供するプロバイダーMAPI では、既定値が用意されていません。 
  
MAPI では、 **PR_DISPLAY_TYPE**フォルダーとアドレス帳コンテナーの階層テーブルで使用される他のユーザーの有効なされているいくつかの多くの値を定義します。 通常、フォルダーの**PR_DISPLAY_TYPE**は、別のフォルダーへのリンクを表すアイコンを示すために DT_FOLDER_LINK または DT_FOLDER_SPECIAL は、アプリケーション固有のアイコンを示すために、既定のフォルダー アイコンを示すために DT_FOLDER に設定されています。 DT_FOLDER_LINK は、検索結果のフォルダーで使用されます。 
  
アドレス帳階層テーブルは、これらの必要な列だけでなく、 **PR_CONTAINER_FLAGS**プロパティを含める必要があります。 **PR_CONTAINER_FLAGS**は、階層内のコンテナーのさまざまな属性を示し、1 つのコンテナーを区別するために使用します。 
  
アドレス帳階層テーブルのオプションのプロパティは、 **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) のプロパティです。
  
メッセージ ストアの階層テーブルの必要な列のセットでこれらのプロパティのとおりです。
  
- **PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS**([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
アドレス帳プロバイダーは MAPI の統合のアドレス帳で必要とされるため、階層テーブルの実装で**IMAPITable**メソッドを次をサポートする必要があります。 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

