---
title: メッセージ ストア プロバイダーでの検索のサポート
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
# <a name="supporting-searches-in-message-store-providers"></a>メッセージ ストア プロバイダーでの検索のサポート

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションには、多くの場合、メッセージ ストア内のメッセージの検索に専念するユーザー インターフェイス コンポーネントがいくつか含まれます。 検索基準は [、IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) インターフェイスで [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) メソッドと [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) メソッドによって指定されます。 
  
クライアントは、メッセージ ストア オブジェクトの **PR_FINDER_ENTRYID** ([PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)プロパティを使用して、検索結果のフォルダーを含むメッセージ ストア内のルート フォルダーを識別します。 検索結果フォルダーは、多くの場合、IPM フォルダー ツリーの一部ではなく、非表示のメッセージ ストアのトップ レベルにあるフォルダーです。
  
メッセージ ストア プロバイダーが永続的な検索結果フォルダーを使用するか、クライアントが PR_FINDER_ENTRYID プロパティに格納されているエントリ識別子を開く際 **に作成するかどうかは、実装** の詳細です。 メッセージ ストア プロバイダーは、メッセージ ストアの作成時に作成される永続的なフォルダーを使用する方がやや簡単です。そのため、フォルダーを開くたびにエントリ識別子を確認して検索結果フォルダーを作成するかどうかを確認する複雑な問題が回避されます。 ただし、すべてのメッセージ ストア プロバイダーがこれを実行できるわけではありません。特に、従来のデータベースに MAPI インターフェイスを提供する読み取り専用のメッセージ ストアまたはストアは、多くの場合、許可されないか、基になるストレージ メカニズムに永続的な検索結果フォルダーを作成できません。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

