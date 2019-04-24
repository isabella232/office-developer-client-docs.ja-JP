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
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344577"
---
# <a name="hierarchy-tables"></a>階層テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
階層テーブルには、メッセージストア内のフォルダーまたはアドレス帳コンテナー内のコンテナーに関する情報が含まれています。 階層テーブルの各行には、1つのフォルダーまたはアドレス帳コンテナーに関する情報が記載された一連の列が含まれています。 階層テーブルは、主にクライアントによって使用され、メッセージストアプロバイダーによって実装され、アドレス帳のツリーを表示するためにアドレス帳プロバイダーによって実装されます。 **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで AB_SUBCONTAINERS フラグが指定されていない場合、サブコンテナーを保持できないコンテナーは、階層テーブルを実装しません。
  
階層テーブルには、次の呼び出しを使用してアクセスできます。
  
- [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)。
    
    - や
    
- [imapiprop:: openproperty](imapiprop-openproperty.md)は、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) をプロパティタグおよび IID_IMAPITable としてインターフェイス識別子として渡します。
    
コンテナーとフォルダーは、テーブルのプロパティを取得するための両方の手法をサポートしている必要があります。 クライアントが選択を必要とするため、サービスプロバイダーがこれらのテーブルにアクセスする方法を1つだけサポートすることは許容されません。 
  
> [!IMPORTANT]
> ストアプロバイダーは、階層テーブルに指定された並べ替え順序セットを優先することは保証されません。 
  
**imapiprop:: openproperty**の呼び出しでは、対応するプロパティ**PR_CONTAINER_HIERARCHY**を開くことにより、階層テーブルにアクセスする必要があります。 **PR_CONTAINER_HIERARCHY**は、フォルダーまたはコンテナーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して取得することはできませんが、 [imapiprop:: getproplist](imapiprop-getproplist.md)メソッドによって返される property tag 配列に含まれています。 
  
 **PR_CONTAINER_HIERARCHY**を使用して、コピー操作から階層テーブルを含めたり除外したりすることもできます。 クライアントが[imapiprop:: CopyTo](imapiprop-copyto.md)の*lpexcludeprops*パラメーターで**PR_CONTAINER_HIERARCHY**を指定している場合、コピー操作では、新しいフォルダーまたはコンテナーは元のフォルダーまたはコンテナーの階層テーブルをサポートしません。 
  
次のプロパティは、階層テーブルで必要な列セットを作成します。
  
|||
|:-----|:-----|
|**PR_COMMENT**([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS**([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME**には、階層の表示に表示されるコンテナーまたはフォルダーの名前が含まれています。 
  
 **PR_ENTRYID**は、このコンテナーまたはフォルダーに関連付けられているエントリ識別子です。 長期のエントリ識別子であることが想定されています。 クライアントと MAPI は、このエントリ識別子を**openentry**に渡して、コンテナーまたはフォルダーを開いたり、 [IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)を呼び出して内容を表示したりできます。 
  
 **PR_DEPTH**は、最上位レベルが0のこのコンテナーまたはフォルダーのインデントレベルを示す数値です。 コンテナーまたはフォルダーが存在する階層の深さが深いほど、 **PR_DEPTH**プロパティの値は高くなります。 クライアントは、 **PR_DEPTH**プロパティを使用して階層テーブルを適切に表示するので、ユーザーは、親と子の関係をはっきりと確認できます。 コンテナーまたはフォルダーの深さは、常に、階層テーブルを実装するコンテナーまたはフォルダーを基準にしています。 
  
 **PR_OBJECT_TYPE**は常に MAPI_ABCONT に設定され、アドレス帳の階層テーブルとフォルダー階層テーブルの MAPI_FOLDER が設定されます。 
  
 **PR_DISPLAY_TYPE**は、コンテナーまたはフォルダーが階層テーブル内でどのように表示されるかに関連する数値です。 主に、コンテナーまたはフォルダーの種類を視覚的に区別するために、表示目的で使用されます。 多くのメッセージストアプロバイダーとアドレス帳プロバイダーでは、さまざまなディスプレイの種類にアイコンが使用されています。 これらのアイコンは、プロバイダーが提供します。MAPI では既定値は提供されません。 
  
MAPI は、 **PR_DISPLAY_TYPE**に対して多数の値を定義します。一部の値はフォルダーに対しては有効であり、アドレス帳コンテナーの階層テーブルで使用されるものもあります。 通常、フォルダーの**PR_DISPLAY_TYPE**は、既定のフォルダーアイコンを示すために DT_FOLDER に設定され、別のフォルダーへのリンクを表すアイコンを示すために DT_FOLDER_LINK、あるいはアプリケーション固有のアイコンを示すために DT_FOLDER_SPECIAL に設定されます。 DT_FOLDER_LINK は、検索結果フォルダーと共に使用されます。 
  
これらの必須列に加えて、アドレス帳階層テーブルに**PR_CONTAINER_FLAGS**プロパティを含める必要があります。 **PR_CONTAINER_FLAGS**は、階層内のコンテナーに関するさまざまな属性を示します。これは、コンテナーと別のコンテナーを区別するために使用されます。 
  
アドレス帳階層テーブルのオプションのプロパティは、 **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) プロパティです。
  
メッセージストア階層テーブルには、必要な列セットにこれらのプロパティが含まれています。
  
- **PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS**([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT**([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD**([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
アドレス帳プロバイダーは、MAPI 統合アドレス帳で必要とされるため、次の**IMAPITable**メソッドを階層テーブル実装でサポートする必要があります。 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

