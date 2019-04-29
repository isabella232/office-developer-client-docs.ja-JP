---
title: 階層ビューアーの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421131"
---
# <a name="writing-a-hierarchy-viewer"></a>階層ビューアーの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
階層ビューアーは、フォルダーとアドレス帳のコンテナー階層テーブルを表示するために使用されるユーザーインターフェイスコンポーネントです。 階層の閲覧者は、さまざまなレベルで階層のメンバーを表示したり、必要に応じて各レベルを拡張して縮小したりできます。
  
container プロパティ**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) は、階層のメンバーが表示されるレベルを制御します。 トップレベルのアドレス帳のコンテナーまたはフォルダーを表すエントリは、 **PR_DEPTH**プロパティが0に設定されています。 このプロパティの値は、シーケンシャルレベルのエントリに対して順次インクリメントされます。 つまり、ユーザーが最上位のコンテナーを選択して展開するときに、 **PR_DEPTH**が1に設定されているすべてのコンテナーを表示します。 ユーザーがこれらのサブコンテナーの1つを展開すると、 **PR_DEPTH**が2に設定されているコンテナーが表示されます。 
  
階層ビューアーでは、異なる深さの範囲がサポートしています。 ビューアーを1つまたは2つのレベルのみに制限することも、複数のレベルをサポートすることもできます。拡張性の高い階層を表示する場合は、優先度を設定することができます。 
  
アドレス帳には、アドレス帳の最上位のコンテナーの階層ビューアーがあります。 
  
 **アドレス帳階層テーブルにアクセスするには**
  
1. [IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出し、null エントリ識別子を渡して、アドレス帳のルートコンテナーを開きます。
    
2. ルートコンテナーの[IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、MAPI アドレス帳の階層テーブルにアクセスします。 
    
 **既定のメッセージストアの階層テーブルにアクセスするには**
  
1. 呼び出し[imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)メッセージストアテーブルにアクセスできます。 
    
2. [spropertyrestriction](spropertyrestriction.md)構造を使用して制限を構築し、 **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティが TRUE に設定されている行だけにテーブルを制限します。 
    
3. [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出し、 **spropertyrestriction**を渡して、既定のメッセージストアを表す行を見つけます。 
    
4. メッセージストアテーブルの既定のメッセージストアの行から**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを渡して、 [imapisession:: openentry](imapisession-openentry.md)を呼び出します。
    
5. メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティを取得します。
    
6. メッセージストアの[IMsgStore:: openentry](imsgstore-openentry.md)メソッドを呼び出して、 **PR_IPM_SUBTREE_ENTRYID**プロパティを渡し、メッセージストアの IPM サブツリーのルートフォルダーを開きます。 
    
7. IPM ルートフォルダーの[IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、その階層テーブルにアクセスします。 
    

