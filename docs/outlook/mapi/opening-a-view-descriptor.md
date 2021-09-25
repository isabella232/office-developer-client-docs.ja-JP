---
title: ビュー記述子を開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d510d1f016da2214c46aadd918a7e3cae1804379
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625148"
---
# <a name="opening-a-view-descriptor"></a>ビュー記述子を開く
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くのフォルダーは、通常のビュー、既定のビュー、または任意の数のカスタマイズされたビューで開く場合があります。 ビューでは、フォルダーの内容を表示する方法について説明します。 通常のビューは、代替ビューがない場合や、フォルダーを初めて開く場合に使用されます。 別のビューが存在する場合は、そのビューを使用してフォルダーを開く必要があります。
  
ビューは、ビュー記述子と呼ばれるメッセージで説明されます。 ビュー記述子は通常、関連付けられたメッセージとして作成され、共通または個人用のビュー フォルダーまたは任意の IPM フォルダーに表示されます。
  
### <a name="to-open-a-view-descriptor"></a>ビュー記述子を開く方法
  
1. [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を呼び出して、フォルダーに関連付けられたコンテンツ テーブルを取得します。 
    
2. ビュー記述子用に予約されているメッセージ クラスを含むメッセージのみを検索する制限を作成し [、IMAPITable::Restrict](imapitable-restrict.md) を呼び出してテーブルを制限し [、IMAPITable::QueryRows](imapitable-queryrows.md) を使用して適切な行を取得します。
    
   フォルダーの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_DEFAULT_VIEW_ENTRYID **(** [PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) プロパティを取得します。 **PR_DEFAULT_VIEW_ENTRYID** には、フォルダーの既定のビュー記述子を含むメッセージのエントリ識別子が含まれている必要があります。 この呼び出しは、フォルダーが [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) と [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)の呼び出しで MAPI_ASSOCIATED フラグの使用をサポートしている場合に成功します。
    
3. ビュー [記述子のエントリ識別子を使用して IMsgStore::OpenEntry](imsgstore-openentry.md) を呼び出して開きます。 
    

