---
title: 階層テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428369"
---
# <a name="hierarchy-tables"></a>階層テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
階層テーブルには、メッセージ ストア内のフォルダー、またはアドレス帳コンテナー内のコンテナーに関する情報が含まれます。 階層テーブルの各行には、1 つのフォルダーまたはアドレス帳コンテナーに関する情報を含む列のセットが含まれています。 階層テーブルは主にクライアントによって使用され、メッセージ ストア プロバイダーによってフォルダーとサブフォルダーのツリーを表示するために実装され、アドレス帳プロバイダーによって実装され、アドレス帳にコンテナーのツリーを表示します。 PR_CONTAINER_FLAGS ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに **AB_SUBCONTAINERS** フラグがない場合に示されるサブコンテナーを保持できないコンテナーは、階層テーブルを実装できません。
  
階層テーブルには、次の呼び出しでアクセスできます。
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Or -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) は、PR_CONTAINER_HIERARCHY **(** [PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) をプロパティ タグとして渡し、IID_IMAPITableをインターフェイス識別子として渡します。
    
コンテナーとフォルダーは、テーブル のプロパティを取得するための両方の手法をサポートしている必要があります。 サービス プロバイダーがこれらのテーブルにアクセスする 1 つの方法のみをサポートできるのは、クライアントが選択肢を持つ必要があるため、受け入れられません。 
  
> [!IMPORTANT]
> ストア プロバイダーは、階層テーブルに指定された並べ替え順序セットを尊重する保証はありません。 
  
**IMAPIProp::OpenProperty** の呼び出しでは、対応するプロパティを開いて階層 **テーブル** にアクセスPR_CONTAINER_HIERARCHY。 フォルダー **PR_CONTAINER_HIERARCHY** コンテナーの [IMAPIProp::GetProps メソッドでは取得できませんが、IMAPIProp::GetPropList](imapiprop-getprops.md)メソッドによって返されるプロパティ タグ配列に含 [](imapiprop-getproplist.md)まれます。 
  
 **PR_CONTAINER_HIERARCHY** を使用して、階層テーブルをコピー操作から含めるか除外することもできます。 クライアントがコピー **操作で** [IMAPIProp::CopyTo](imapiprop-copyto.md)の *lpExcludeProps* パラメーターに PR_CONTAINER_HIERARCHY を指定した場合、新しいフォルダーまたはコンテナーは元のフォルダーまたはコンテナーの階層テーブルをサポートしない。 
  
次のプロパティは、階層テーブルで必要な列セットを構成します。
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** には、階層の表示に表示するコンテナーまたはフォルダーの名前が含まれます。 
  
 **PR_ENTRYID** は、このコンテナーまたはフォルダーに関連付けられているエントリ識別子です。 これは、長期的なエントリ識別子である必要があります。 クライアントと MAPI は、このエントリ識別子を **OpenEntry** に渡してコンテナーまたはフォルダーを開き [、IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を呼び出すことによってその内容を表示できます。 
  
 **PR_DEPTH** は、このコンテナーまたはフォルダーのインデントのレベルを表す数値で、0 がトップ レベルです。 コンテナーまたはフォルダーが存在する階層が深いほど、コンテナーまたはフォルダーのプロパティの値 **PR_DEPTH** します。 クライアントは **、PR_DEPTH** プロパティを使用して階層テーブルを適切に表示し、ユーザーが親と子の関係を明確に確認できます。 コンテナーまたはフォルダーの深度は、階層テーブルを実装するコンテナーまたはフォルダーに対して常に相対的です。 
  
 **PR_OBJECT_TYPE** は、常にアドレス帳MAPI_ABCONTテーブルとフォルダー階層テーブルのMAPI_FOLDERに設定されます。 
  
 **PR_DISPLAY_TYPE** は、コンテナーまたはフォルダーを階層テーブルに表示する方法に関連する数値です。 これは主に、コンテナーまたはフォルダーの種類を視覚的に区別するために、表示目的で使用されます。 多くのメッセージ ストアプロバイダーとアドレス帳プロバイダーは、さまざまな種類の表示にアイコンを使用します。 これらのアイコンはプロバイダーが提供する必要があります。MAPI では、既定値は指定されません。 
  
MAPI では、アドレス帳コンテナー PR_DISPLAY_TYPE階層テーブルで使用されるフォルダーや他のフォルダーに有効な値を多数定義します。 通常、フォルダーの **PR_DISPLAY_TYPE** は DT_FOLDER に設定して既定のフォルダー アイコンを示し、DT_FOLDER_LINK は別のフォルダーへのリンクを表すアイコンを示し、DT_FOLDER_SPECIAL はアプリケーション固有のアイコンを示します。 DT_FOLDER_LINKは、検索結果フォルダーと一緒に使用されます。 
  
これらの必須の列に加えて、アドレス帳階層テーブルに PR_CONTAINER_FLAGSする **必要** があります。 **PR_CONTAINER_FLAGS** は、階層内のコンテナーに関するさまざまな属性を示し、あるコンテナーを別のコンテナーと区別するために使用されます。 
  
アドレス帳階層テーブルの省略可能なプロパティは、PR_AB_PROVIDER_ID **(** [PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) プロパティです。
  
メッセージ ストア階層テーブルには、必要な列セットに次のプロパティが含まれます。
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
アドレス帳プロバイダーは、MAPI 統合アドレス帳で必要なので、階層テーブルの実装で次の **IMAPITable** メソッドをサポートする必要があります。 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

