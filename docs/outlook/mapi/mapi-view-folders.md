---
title: MAPI フォルダーの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cb26771e9968175ab67366e35cf019ce23d51b8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801483"
---
# <a name="mapi-view-folders"></a>MAPI フォルダーの表示

  
  
**適用対象**: Outlook 
  
フォルダーの表示は、個人間メッセージ (IPM) のフォルダーの内容の別の表示のレイアウトを定義するのには関連する情報を含むルート フォルダーです。 フォルダーの表示では、メッセージ ・ ストアのルートの下に存在する、したがって、一般的なクライアント アプリケーションで表示されているではありません。 すべてのメッセージ ストアには、フォルダー表示; にはが含まれています。セッションの既定のメッセージ ストアとして機能するように構成されている唯一のメッセージ ・ ストアには、それらを含める必要があります。  
  
MAPI には、2 つのフォルダーの表示がサポートされています。
  
- 共通、共通のフォルダー ビューにはには、メッセージ ・ ストアの標準であり、メッセージ ・ ストアにアクセスするクライアントのすべてのユーザーが使用できるビューが含まれています。 一般的なビュー フォルダーのエントリ id は、店舗の**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) のプロパティに格納されます。
    
- 個人、個人用ビューのフォルダーには、特定のユーザーが定義されているビューが含まれています。 MAPI では、個人用ビューのフォルダーのエントリ id を保持するための**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) のプロパティを定義します。 個人用ビューを使用すると、たとえば、1 人のユーザー可能性があります見てメッセージの送信者にのみメッセージ件名および受入日付を一覧表示順のグループ他のユーザー、件名、送信者、およびメッセージのサイズを一覧表示、日付で並べ替えられた同じグループになります。
    
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

