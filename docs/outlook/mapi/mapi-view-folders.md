---
title: MAPI 表示フォルダー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ca9e5138d3ded13dfe33037f75e43ef1098f3c2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412535"
---
# <a name="mapi-view-folders"></a>MAPI 表示フォルダー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの表示は、関連情報が含まれているルートフォルダーで、個人間メッセージ (IPM) フォルダーの内容の代替の表示レイアウトを定義します。 表示フォルダーは、メッセージストアのルートの下に存在するため、一般的なクライアントアプリケーションでは表示されません。 すべてのメッセージストアに表示フォルダーが含まれているわけではありません。セッションの既定のメッセージストアとして機能するように構成されたメッセージストアのみを含める必要があります。  
  
MAPI は、2つの表示フォルダーをサポートします。
  
- common: common view フォルダーには、メッセージストアの標準のビューが含まれており、メッセージストアにアクセスするクライアントの任意のユーザーが使用できます。 共通ビューフォルダーのエントリ識別子は、ストアの**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) プロパティに格納されます。
    
- personal —個人用ビューフォルダーには、特定のユーザーによって定義されたビューが含まれています。 MAPI は、個人用ビューフォルダーのエントリ識別子を保持するための**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) プロパティを定義します。 個人用ビューを使用すると、たとえば1人のユーザーが、メッセージの件名と受信日のみを一覧表示し、送信者によって並べ替えられたメッセージのグループを確認できます。別のユーザーは、日付で並べ替えられた同じグループを調べ、件名、送信者、およびメッセージサイズを一覧表示することができます。
    
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

