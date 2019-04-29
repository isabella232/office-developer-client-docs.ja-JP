---
title: メッセージストアプロバイダーでの検索のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425387"
---
# <a name="supporting-searches-in-message-store-providers"></a>メッセージストアプロバイダーでの検索のサポート

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多くの場合、クライアントアプリケーションには、メッセージストア内のメッセージを検索するために使用されるユーザーインターフェイスコンポーネントがいくつかあります。 検索条件は、 [IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドと[IMAPIContainer:: getsearchcriteria](imapicontainer-getsearchcriteria.md)メソッドを使って、 [IMAPIContainer: imapiprop](imapicontainerimapiprop.md)インターフェイスで指定します。 
  
クライアントは、メッセージストアオブジェクトの**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) プロパティを使用して、検索結果のフォルダーが格納されているメッセージストア内のルートフォルダーを特定します。 検索結果フォルダーは、多くの場合、メッセージストアの最上位レベルにあるフォルダーで、IPM フォルダーツリーには含まれていないため、非表示になります。
  
メッセージストアプロバイダーが永続的な検索結果フォルダーを使用するか、クライアントが開くときに1つを作成するかどうかは、 **PR_FINDER_ENTRYID**プロパティに格納されているエントリ識別子が実装の詳細です。 メッセージストアプロバイダーでは、メッセージストアの作成時に作成されたパーマネントフォルダーを使用する方が簡単です。これにより、フォルダーが開かれるたびにエントリ識別子をチェックして、を作成するかどうかを確認するのが困難になります。検索結果フォルダー。 ただし、すべてのメッセージストアプロバイダーがこれを実行できるわけではありません。特に、従来のデータベースに MAPI インターフェイスを提供する読み取り専用のメッセージストアまたはストアは、基礎となるストレージメカニズムでは、通常は許可されていないか、または永続的な検索結果フォルダーを作成できません。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

