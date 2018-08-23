---
title: ビュー記述子を開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 680d80c0827399f3b7a0ea5819e51be654a05810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592480"
---
# <a name="opening-a-view-descriptor"></a>ビュー記述子を開く
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
標準表示モード、既定のビューまたは個人用ビューの任意の数に多くのフォルダーを開くことができます。 ビューでは、フォルダーの内容を表示する方法について説明します。 標準のビューは、別のビューがない場合に、最初にフォルダーを開くときに使用されます。 代替ビューが存在する場合は、フォルダーを開くに使用してください。
  
ビューは、ビュー記述子と呼ばれるメッセージの説明です。 ビュー記述子では、通常、関連付けられているメッセージとして作成し、[共通] または [個人用のビュー フォルダーまたは IPM の任意のフォルダー内に表示されます。
  
### <a name="to-open-a-view-descriptor"></a>ビュー記述子を開く
  
1. フォルダーの内容を関連するテーブルを取得するために[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を呼び出します。 
    
2. ビュー記述子用に予約されたメッセージ クラスのメッセージだけを検索する制限を作成し、テーブルを制限する[IMAPITable::Restrict](imapitable-restrict.md)と、適切な行を取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出すか、.
    
   **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) のプロパティを取得するために、フォルダーの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。 **PR_DEFAULT_VIEW_ENTRYID**には、フォルダーの既定のビューの記述子が含まれるメッセージのエントリ id が含まれています。 フォルダーは、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)および[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)への呼び出しに MAPI_ASSOCIATED フラグの使用をサポートしている場合、この呼び出しは成功します。
    
3. 開くビュー記述子のエントリの識別子を使用して[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 
    

