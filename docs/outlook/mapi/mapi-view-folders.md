---
title: MAPI ビュー フォルダー
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
# <a name="mapi-view-folders"></a>MAPI ビュー フォルダー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ビュー フォルダーは、関連情報を含むルート フォルダーで、対人間メッセージ (IPM) フォルダーのコンテンツの代替表示レイアウトを定義します。 ビュー フォルダーはメッセージ ストアのルートの下に存在するため、一般的なクライアント アプリケーションには表示されません。 すべてのメッセージ ストアにビュー フォルダーが含まれる場合があります。セッションの既定のメッセージ ストアとして動作するように構成されているメッセージ ストアだけが、それらを含める必要があります。  
  
MAPI では、次の 2 つのビュー フォルダーがサポートされています。
  
- Common — 共通ビュー フォルダーには、メッセージ ストアに標準のビューが含まれているので、メッセージ ストアにアクセスするクライアントの任意のユーザーが使用できます。 共通ビュー フォルダーのエントリ識別子は、ストアのプロパティ **(** [PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) PR_COMMON_VIEWS_ENTRYIDに格納されます。
    
- 個人用 - 個人用ビュー フォルダーには、特定のユーザーによって定義されたビューが含まれる。 MAPI では、個人用 **PR_VIEWS_ENTRYID** のエントリ識別子を保持するプロパティ [(PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)プロパティを定義します。 たとえば、個人用ビューを使用すると、1 人のユーザーが送信者別に並べ替えたメッセージのグループを確認し、メッセージの件名と受信日のみを一覧に表示できます。別のユーザーは、日付順に並べ替えた同じグループを見て、件名、送信者、メッセージ サイズを一覧に表示できます。
    
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

