---
title: MAPI ビュー フォルダー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 194d62a645a5c641abc931db695b0d6acf0ac53a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579496"
---
# <a name="mapi-view-folders"></a>MAPI ビュー フォルダー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ビュー フォルダーは、関連情報を含むルート フォルダーで、対人間メッセージ (IPM) フォルダーのコンテンツの代替表示レイアウトを定義します。 ビュー フォルダーはメッセージ ストアのルートの下に存在するため、一般的なクライアント アプリケーションには表示されません。 すべてのメッセージ ストアにビュー フォルダーが含まれる場合があります。セッションの既定のメッセージ ストアとして動作するように構成されているメッセージ ストアだけが、それらを含める必要があります。  
  
MAPI では、次の 2 つのビュー フォルダーがサポートされています。
  
- Common — 共通ビュー フォルダーには、メッセージ ストアに標準のビューが含まれているので、メッセージ ストアにアクセスするクライアントの任意のユーザーが使用できます。 共通ビュー フォルダーのエントリ識別子は、ストアのプロパティ **(** [PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) PR_COMMON_VIEWS_ENTRYIDに格納されます。
    
- 個人用 - 個人用ビュー フォルダーには、特定のユーザーによって定義されたビューが含まれる。 MAPI では、個人用 **PR_VIEWS_ENTRYID** のエントリ識別子を保持するプロパティ [(PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)プロパティを定義します。 たとえば、個人用ビューを使用すると、1 人のユーザーが送信者別に並べ替えたメッセージのグループを確認し、メッセージの件名と受信日のみを一覧に表示できます。別のユーザーは、日付順に並べ替えた同じグループを見て、件名、送信者、メッセージ サイズを一覧に表示できます。
    
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

