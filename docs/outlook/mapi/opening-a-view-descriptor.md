---
title: ビュー記述子を開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326209"
---
# <a name="opening-a-view-descriptor"></a>ビュー記述子を開く
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常のビュー、既定のビュー、または任意の数の個人用ビューを使用して、多くのフォルダーを開くことができます。 ビューは、フォルダーの内容を表示する方法について説明します。 標準表示モードは、代替ビューがない場合、またはフォルダーを初めて開いたときに使用されます。 代替ビューが存在する場合は、それを使用してフォルダーを開く必要があります。
  
ビューは、ビュー記述子と呼ばれるメッセージで記述されます。 通常は、関連付けられたメッセージとして作成され、[共通] または [個人用ビュー] フォルダーまたは任意の IPM フォルダーに表示することができます。
  
### <a name="to-open-a-view-descriptor"></a>ビュー記述子を開くには
  
1. [IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)を呼び出して、フォルダーの関連付けられたコンテンツテーブルを取得します。 
    
2. ビュー記述子に予約されたメッセージクラスを持つメッセージのみを特定する制限[](imapitable-restrict.md)を作成し、次のように、適切な行を取得するには、テーブルと imapitable:: [QueryRows](imapitable-queryrows.md)を制限します。
    
   フォルダーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、その**PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) プロパティを取得します。 **PR_DEFAULT_VIEW_ENTRYID**には、フォルダーの既定のビュー記述子を含むメッセージのエントリ識別子が含まれています。 フォルダーが[imapifolder:: CreateMessage](imapifolder-createmessage.md)および[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)への呼び出しで MAPI_ASSOCIATED フラグの使用をサポートしている場合、この呼び出しは成功します。
    
3. を開くには、 [IMsgStore:: openentry](imsgstore-openentry.md)という名前のビュー記述子のエントリ識別子を使用します。 
    

