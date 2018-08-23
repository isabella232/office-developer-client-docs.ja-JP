---
title: メッセージ ストア プロバイダーでの検索のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f206623103f810b2868502aea7c6804cd306f022
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573195"
---
# <a name="supporting-searches-in-message-store-providers"></a>メッセージ ストア プロバイダーでの検索のサポート

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアント アプリケーションでは、メッセージ ・ ストア内のメッセージを検索するのには熱心なユーザー インターフェイス コンポーネントがいくつかが頻繁にあります。 検索条件が指定の[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) 、 [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)および[IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md)メソッドを使用してインターフェイスです。 
  
クライアントは、検索結果のフォルダーを含むメッセージ ストアのルート フォルダーを識別するのには、メッセージ ストア オブジェクトの**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) のプロパティを使用します。 検索結果フォルダーは、多くの場合、IPM のフォルダー ツリーの一部ではないと、そのため、非表示になっているメッセージ ストアの最上部にあるフォルダーです。
  
メッセージ ストア プロバイダーが検索結果の永続的なフォルダーを使用して、またはクライアントを開くと、 **PR_FINDER_ENTRYID**プロパティに格納されているエントリの識別子を作成するかどうかは、実装の詳細です。 エントリの識別子を作成するかどうかを確認するのには任意のフォルダーを開くたびにチェックの問題を避けることができますので、メッセージ ストアを作成するときに作成される永続的なフォルダーを使用するのには、メッセージ ストア プロバイダーをいくらか簡単には、検索結果のフォルダーです。 ただし、すべてのメッセージ ストア プロバイダーが行うことです。特に、読み取り専用のメッセージ ストアまたは多くの場合、従来のデータベースに MAPI インターフェイスを提供するストアは許可されていませんか、基になるストレージ機構で検索結果の永続的なフォルダーを作成することができません。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

